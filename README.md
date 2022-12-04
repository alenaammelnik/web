# code 

using UnityEngine;
using System.Collections;

public class Shooter : MonoBehaviour
{
	public GameObject cubePrefab;
	// Update is called once per frame
	void Update () 
	{
		if (Input.GetButtonDown("Jump"))
		{
			GameObject cube = Instantiate(cubePrefab, transform.position, transform.rotation) as GameObject; 
			cube.rigidbody.AddForce(transform.forward * 1000);
		}
	}
}
