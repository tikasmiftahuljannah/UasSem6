import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: LoginPage(),
    );
  }
}

class LoginPage extends StatefulWidget {
  LoginPageState createState() => LoginPageState();
}

class LoginPageState extends State<LoginPage> {
  final txtuser = TextEditingController();
  String nUsername, nPassword;

  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Tika S. Miftahul Jannah'),
      ),
      body: Padding(
        padding: EdgeInsets.only(left: 42, right: 42, top: 32, bottom: 32),
        child: Column(
          mainAxisSize: MainAxisSize.min,
          children: <Widget>[
            Padding(
              padding: const EdgeInsets.only(bottom: 32),
            ),
            TextField(
              controller: txtuser,
              decoration: InputDecoration(
                   
                  hintText: 'Input Nama Depan Mahasiswa',
                  border: OutlineInputBorder(
                      borderRadius: BorderRadius.all(Radius.circular(32)))),
            ),
            
            Padding(
              padding: const EdgeInsets.only(top: 0),
              child: Container(
                width: 200,
                height: 40,
                margin: EdgeInsets.only(top: 32),
                decoration: BoxDecoration(
                    color: Color(0XFF2a3ed7),
                    borderRadius: BorderRadius.all(Radius.circular(50))),
                child: Center(
                  child: TextButton(
                    onPressed: () {
                      nUsername = txtuser.text;

                      if (nUsername == "Tika")
                        Navigator.push(context,
                            MaterialPageRoute(builder: (context) => Utama()));
                    },
                    child: Text('Login', style: TextStyle(
                color: Colors.grey, fontWeight: FontWeight.bold),),
                  ),
                ),
              ),
            ),
          ],
        ),
      ),
    );
  }
}

class Utama extends StatelessWidget {
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      routes: {
        '/Data Mahasiswa' :(BuildContext context) => new Data(),
        '/Perhitungan' :(BuildContext context) => new ProgramMatematika(),
      },
      
      
      home: Scaffold(
        backgroundColor: Colors.white,
        appBar: AppBar(
          title: Text('Menu Utama '),
          backgroundColor: Colors.purple,
        ),
        //body
        body: GridView.count(
          crossAxisCount: 2,
          children: <Widget>[
            MyMenu(judul: "Data Mahasiswa", icon: Icons.assignment_ind),
            MyMenu(judul: "Perhitungan", icon: Icons.point_of_sale),
          ],
        ),
      ),
    );
  }
}

class MyMenu extends StatelessWidget {
  //Atribut
  final String judul;
  final IconData icon;
  final MaterialColor warna;
  //constructor
  MyMenu({this.judul, this.icon, this.warna});

  Widget build(BuildContext context) {
    return Card(
      margin: EdgeInsets.all(8.0),
      child: InkWell(
        onTap: () {Navigator.pushNamed(context, '/$judul');},
        splashColor: Colors.deepPurpleAccent,
        child: Center(
          child: Column(
            mainAxisSize: MainAxisSize.min,
            children: <Widget>[
              Icon(icon, size:50.0),
              Text(judul, style: new TextStyle(fontSize: 17.0))
            ],
          ),
        ),
      ),
    );
  }
}

class Data extends StatelessWidget {
  Widget build(BuildContext context) {
    return new Scaffold(
      appBar: new AppBar(
        title: new Text("Data Mahasiswa"),
      ),
      body: new Column(
        children: <Widget>[
          new ListTile(
            subtitle: const Text('Nama Mahasiswa'),
            title: const Text('Tika S. Miftahul Jannah'),
          ),
          new ListTile(
            subtitle: const Text('Nirm'),
            title: const Text('2018020030'),
          ),
           new ListTile(
            subtitle: const Text('Matakuliah'),
            title: const Text('Pemograman Mobile'),
             ),
           new ListTile(
            subtitle: const Text('Jurusan'),
            title: const Text('Sistem Informasi'),
          ),
          new ListTile(
            subtitle: const Text('Aplikasi ini dibuat untuk memenuhi tugas UAS '),
            
          ),
        ],
      ),
    );
  }
}

class ProgramMatematika extends StatefulWidget {
  createState() => _ProgramMatematikaInputDataState();
}

class _ProgramMatematikaInputDataState extends State<ProgramMatematika> {
  
  
  final _panjang = TextEditingController();
  final _lebar = TextEditingController();
  String _hasil='';
 

  onHitung() {
    setState(() {
      var hitung= int.parse(_panjang.text)* int.parse( _lebar .text);
      _hasil =
         "hasil = $hitung cm";
    });
  }

  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        backgroundColor: Colors.blue,
        title: Text("Program Menghitung Luas"),
      ),
      body: Container(
        padding: EdgeInsets.all(20.0),
        child: Column(
          children: [
             TextField(
              controller: _panjang,
              decoration: InputDecoration(labelText: "Input Panjang"),
            ),
            TextField(
              controller: _lebar,
              decoration: InputDecoration(labelText: "Input Lebar"),
            ),
            RaisedButton(
              child: Text("Hitung"),
              onPressed: onHitung,
            ),
            Text("$_hasil"),
          ],
        ),
      ),
    );
  }
}
class Gagal extends StatelessWidget {
  Widget build(BuildContext context) {
    return Scaffold(
        backgroundColor: Colors.black,
        appBar: AppBar(
          title: Text(
            " GAGAL LOGIN ",
          ),
        ),
        body: Center(child: Text("ANDA GAGAL LOGIN !!!!", style: TextStyle(color: Colors.red, fontWeight: FontWeight.bold))));
  }
}
