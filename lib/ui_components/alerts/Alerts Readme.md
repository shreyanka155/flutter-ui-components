<h1 align=center> Flutter UI Components (Under Development) </h1>
<h3 align=center> Amazing UI Components for you to choose from. 📜 </h3>
<h3 align=center> ALERTS</h3>
<p align=center>
  Alert components are elements that are used to inform users about important events, messages, or updates within a website or application. These notifications can take various forms, such as alert banners, pop-up messages, or badges, and may contain text, graphics, or other types of media. Notification components are often used to communicate important information to users, such as errors, warnings, or alerts, or to provide updates on the status of a task or process. They can be designed to be persistent or temporary, and may include actions or buttons that allow users to interact with them.
</p>

<table>
  <tr>
    <td></td>
    <td>Screen Shots</td>
    <td>Code snippets</td>
  </tr>
  <tr>
    <td>1.</td>
    <td><img src="https://github.com/Clueless-Community/flutter-ui-components/blob/main/assets/Screenshots/banner.jpg" width=400 height=500></td>
    <td>
    
```flutter

  import 'package:flutter/material.dart';
import 'package:google_fonts/google_fonts.dart';

class Alert1 extends StatefulWidget {
  const Alert1({super.key});

  @override
  State<Alert1> createState() => _Alert1State();
}

class _Alert1State extends State<Alert1> {
  late bool _visible = true;
  @override
  Widget build(BuildContext context) {
    return AnimatedOpacity(
      opacity: _visible ? 1.0 : 0.0,
      duration: const Duration(milliseconds: 500),
      child: Container(
        padding: const EdgeInsets.symmetric(horizontal: 15),
        height: 68,
        width: double.infinity,
        decoration: BoxDecoration(
            color: const Color.fromRGBO(206, 24, 33, 1),
            borderRadius: BorderRadius.circular(8)),
        child: Row(
          children: [
            const Icon(
              Icons.info,
              color: Colors.white,
            ),
            const SizedBox(
              width: 15,
            ),
            Expanded(
              child: Column(
                mainAxisAlignment: MainAxisAlignment.center,
                crossAxisAlignment: CrossAxisAlignment.start,
                children: [
                  Text(
                    'Message',
                    style: TextStyle(
                        fontFamily:
                            GoogleFonts.publicSans(fontWeight: FontWeight.w600)
                                .fontFamily,
                        fontSize: 18,
                        color: Colors.white),
                  ),
                  Text('Description',
                      style: TextStyle(
                          fontFamily: GoogleFonts.publicSans(
                                  fontWeight: FontWeight.w400)
                              .fontFamily,
                          fontSize: 18,
                          color: Colors.white)),
                ],
              ),
            ),
            InkWell(
              onTap: () {
                setState(() {
                  _visible = !_visible;
                });
              },
              child: const Icon(
                Icons.cancel_sharp,
                color: Colors.white,
              ),
            )
          ],
        ),
      ),
    );
  }
}

```

</td>
  </tr>
</table>
