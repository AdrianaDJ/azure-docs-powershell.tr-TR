---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: e93efdaf8ec55c3b7c8fb0793a24e062553545ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274466"
---
# <span data-ttu-id="0c35f-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0c35f-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="0c35f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c35f-102">SYNOPSIS</span></span>
<span data-ttu-id="0c35f-103">Kaynak grubunda bir mantık uygulaması çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="0c35f-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="0c35f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c35f-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c35f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c35f-105">DESCRIPTION</span></span>
<span data-ttu-id="0c35f-106">**Start-Azlogicuyg** cmdlet 'ı, mantık uygulamaları özelliğini kullanarak bir mantık uygulaması çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="0c35f-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="0c35f-107">Bir ad, kaynak grubu ve tetik belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c35f-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="0c35f-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="0c35f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0c35f-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="0c35f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0c35f-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="0c35f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0c35f-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="0c35f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0c35f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c35f-112">EXAMPLES</span></span>

### <span data-ttu-id="0c35f-113">Örnek 1: mantık uygulaması Çalıştır</span><span class="sxs-lookup"><span data-stu-id="0c35f-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="0c35f-114">Bu komut, ResourceGroup11 adlı kaynak grubundaki mantık uygulamasını çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="0c35f-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="0c35f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c35f-115">PARAMETERS</span></span>

### <span data-ttu-id="0c35f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c35f-116">-DefaultProfile</span></span>
<span data-ttu-id="0c35f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0c35f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c35f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c35f-118">-Name</span></span>
<span data-ttu-id="0c35f-119">Bu cmdlet 'in başladığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c35f-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c35f-120">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="0c35f-120">-Parameters</span></span>
<span data-ttu-id="0c35f-121">Mantık uygulamasının parametre koleksiyonu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c35f-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="0c35f-122">Karma tablo, sözlük \<string\> veya sözlük belirtin \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="0c35f-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c35f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c35f-123">-ResourceGroupName</span></span>
<span data-ttu-id="0c35f-124">Bu cmdlet 'in başladığı mantık uygulamasını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c35f-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c35f-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="0c35f-125">-TriggerName</span></span>
<span data-ttu-id="0c35f-126">Bu cmdlet 'in başladığı mantık uygulamasının tetikleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c35f-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c35f-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c35f-127">-Confirm</span></span>
<span data-ttu-id="0c35f-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c35f-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c35f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c35f-129">-WhatIf</span></span>
<span data-ttu-id="0c35f-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c35f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c35f-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c35f-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c35f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c35f-132">CommonParameters</span></span>
<span data-ttu-id="0c35f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c35f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c35f-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c35f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c35f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c35f-135">INPUTS</span></span>

### <span data-ttu-id="0c35f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0c35f-136">System.String</span></span>

## <span data-ttu-id="0c35f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c35f-137">OUTPUTS</span></span>

### <span data-ttu-id="0c35f-138">System. void</span><span class="sxs-lookup"><span data-stu-id="0c35f-138">System.Void</span></span>

## <span data-ttu-id="0c35f-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c35f-139">NOTES</span></span>

## <span data-ttu-id="0c35f-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c35f-140">RELATED LINKS</span></span>

[<span data-ttu-id="0c35f-141">Get-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="0c35f-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="0c35f-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="0c35f-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="0c35f-143">Yeni-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="0c35f-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="0c35f-144">Remove-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="0c35f-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="0c35f-145">Set-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="0c35f-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="0c35f-146">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="0c35f-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


