---
title: The Worst Snake Ever
layout: post
author: harry.keyland
permalink: /untitled-document/
source-id: 1Crn_MOtZeiZtPWjSP4fwu2BQEngRdwL7xCh2fFyMHdg
published: true
---
function onStart(  ) {

	globals.Score = 1000;

	globals.PosX = 0;

	globals.PosY = 4;

	globals.AppleX = 4;

	globals.AppleY = 3;

	globals.Level = 0;

	while (globals.Level < 10) {

		

		microbit.on(globals.PosX, globals.PosY);

		wait(100);

		microbit.off(globals.PosX, globals.PosY);

		wait(100);

		microbit.on(globals.PosX, globals.PosY);

		microbit.off(globals.AppleX, globals.AppleY);

		

	}

	

	if (globals.PosX == ( globals.AppleY && ( globals.PosY == globals.AppleY ) )) {

		

		microbit.draw(Pattern("01010.01010.00000.10001.01110"));

		wait(300);

		globals.Level = globals.Level + 1;

		globals.AppleX = Random.number(0, 4);

		globals.AppleY = Random.number(0, 4);

		microbit.clear();

		

	}

	

	if (microbit.tiltX > ( 2 && ( globals.PosX >= 1 ) )) {

		

		microbit.off(globals.PosX, globals.PosY);

		globals.PosX = globals.PosX - 1;

		

	}

	

	if (microbit.tiltX < ( 2 && ( globals.PosX <= 3 ) )) {

		

		microbit.off(globals.PosX, globals.PosY);

		globals.PosX = globals.PosX + 1;

		

	}

	

	if (microbit.tiltY > ( 2 && ( globals.PosY >= 1 ) )) {

		

		microbit.off(globals.PosX, globals.PosY);

		globals.PosY = globals.PosY - 1;

		

	}

	

	if (microbit.tiltY < ( 2 && ( globals.PosY <= 3 ) )) {

		

		microbit.off(globals.PosY, globals.PosX);

		globals.PosY = globals.PosY + 1;

		

	}

	

	globals.Score = globals.Score - 1;

	microbit.say(globals.Score);

