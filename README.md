# ThoughtWorks

package com.example.demo.model;

import java.util.Arrays;

import org.apache.http.client.HttpClient;
import org.apache.http.client.methods.HttpGet;
import org.apache.http.impl.client.DefaultHttpClient;
import org.springframework.http.*;
import org.springframework.http.MediaType;
import com.mashape.unirest.http.HttpResponse;
import com.mashape.unirest.http.Unirest;
import com.mashape.unirest.http.exceptions.UnirestException;
import org.springframework.web.client.RestTemplate;
public class Encrypt {

	public static void main(String[] args) {
		/*String foo = "GOVV GO MKX NY SD WI GKI, YB GO MKX KVV MYWO LKMU SX DSWO PYB DRO XOHD KVSQXWOXD KXN IYE'BO GOVMYWO DY DBI KXN USVV WO DROX, SX YR, CKI, KXYDROB 5,000 IOKBC?";
		String bar = "";

		for (char c : foo.toCharArray()) {
			if ((c >= 65 && c <= 122)) 
			{
				int test=	(((c - 'A' - 10) % 26) + 'A');
				if(test<65)
				{
					int tuf=0;
					tuf=(65-test);
					test='Z'-(65-test)+1;
					//test='Z'-cha;
				}
				// bar += Character.toString((char) (((c - 'A' - 5) % 26) + 'A'));
				bar += Character.toString((char) test);
			}
			else 
				bar+=Character.toString(c);
		}


		System.out.println(bar);*/
		HttpHeaders headers = new HttpHeaders();
		 
        // Request to return JSON format
        headers.setContentType(MediaType.APPLICATION_JSON);
        headers.set("userid", "IOTVYB8bc");
        headers.set("postman-token", "51cda29c-0d59-2fa4-5591-edca4149eb38");
        HttpEntity<String> entity = new HttpEntity<String>(headers);
        RestTemplate restTemplate = new RestTemplate();
        Input result= restTemplate.getForObject("http://http-hunt.thoughtworks-labs.net/challenge", Input.class,entity);
     /*   ResponseEntity<Input> response = restTemplate.exchange("http://http-hunt.thoughtworks-labs.net/challenge/input", //
                HttpMethod.GET, entity, Input.class);*/
        
 
      //  Input result = response.getBody();
        System.out.println(result);
		/*try {
			HttpResponse<Input> response = Unirest.get("http://http-hunt.thoughtworks-labs.net/challenge/input")
					.header("UserID", "IOTVYB8bc")
					.header("content-type", "application/json")
					.header("cache-control", "no-cache")
					.asObject(Input.class);
			System.out.println(response.getBody());;
			
		} catch (UnirestException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}*/
	}

}
