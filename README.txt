// ��� ��


import kr.studio321.aheui.Lexer;
import kr.studio321.aheui.Machine;

var code:String = "��P�����P�����\n" +
"�����Ļ��޹�ѹ�\n" +
"���U�����ĔƵκ�\n" +
"�����ڹߌ�������\n" +
"��������ݹ�����\n" +
"���K��������Ѷ�\n" +
"�̻Ǹݸݴ�������\n" +
"�ǵ����ݻ�������\n";

var machine:Machine = new Machine;
machine.codeSpace = Lexer.tokenize( code );

while( machine.state )
{
	machine.step();
}

trace( machine.output );