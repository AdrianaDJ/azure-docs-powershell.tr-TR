---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: 1ec020aa93b1a7e6964e8f85eb8a02c6a9f895cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915927"
---
# <span data-ttu-id="8aff2-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8aff2-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="8aff2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aff2-102">SYNOPSIS</span></span>
<span data-ttu-id="8aff2-103">Kaynak grubunda bir mantık uygulaması çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="8aff2-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="8aff2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8aff2-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8aff2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8aff2-105">DESCRIPTION</span></span>
<span data-ttu-id="8aff2-106">**Start-Azlogicuyg** cmdlet 'ı, mantık uygulamaları özelliğini kullanarak bir mantık uygulaması çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="8aff2-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="8aff2-107">Bir ad, kaynak grubu ve tetik belirtin.</span><span class="sxs-lookup"><span data-stu-id="8aff2-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="8aff2-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="8aff2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8aff2-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="8aff2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8aff2-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="8aff2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8aff2-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="8aff2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8aff2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8aff2-112">EXAMPLES</span></span>

### <span data-ttu-id="8aff2-113">Örnek 1: mantık uygulaması Çalıştır</span><span class="sxs-lookup"><span data-stu-id="8aff2-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="8aff2-114">Bu komut, ResourceGroup11 adlı kaynak grubundaki mantık uygulamasını çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="8aff2-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="8aff2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8aff2-115">PARAMETERS</span></span>

### <span data-ttu-id="8aff2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aff2-116">-DefaultProfile</span></span>
<span data-ttu-id="8aff2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8aff2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8aff2-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="8aff2-118">-Name</span></span>
<span data-ttu-id="8aff2-119">Bu cmdlet 'in başladığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8aff2-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="8aff2-120">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="8aff2-120">-Parameters</span></span>
<span data-ttu-id="8aff2-121">Mantık uygulamasının parametre koleksiyonu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8aff2-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="8aff2-122">Karma tablo, sözlük \< dizesi \> veya sözlük \< dizesi, WorkflowParameter belirtin \> .</span><span class="sxs-lookup"><span data-stu-id="8aff2-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="8aff2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aff2-123">-ResourceGroupName</span></span>
<span data-ttu-id="8aff2-124">Bu cmdlet 'in başladığı mantık uygulamasını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8aff2-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="8aff2-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="8aff2-125">-TriggerName</span></span>
<span data-ttu-id="8aff2-126">Bu cmdlet 'in başladığı mantık uygulamasının tetikleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8aff2-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="8aff2-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="8aff2-127">-Confirm</span></span>
<span data-ttu-id="8aff2-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8aff2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aff2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aff2-129">-WhatIf</span></span>
<span data-ttu-id="8aff2-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8aff2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8aff2-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8aff2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aff2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aff2-132">CommonParameters</span></span>
<span data-ttu-id="8aff2-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8aff2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aff2-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8aff2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aff2-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8aff2-135">INPUTS</span></span>

### <span data-ttu-id="8aff2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8aff2-136">System.String</span></span>

## <span data-ttu-id="8aff2-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8aff2-137">OUTPUTS</span></span>

### <span data-ttu-id="8aff2-138">System. void</span><span class="sxs-lookup"><span data-stu-id="8aff2-138">System.Void</span></span>

## <span data-ttu-id="8aff2-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8aff2-139">NOTES</span></span>

## <span data-ttu-id="8aff2-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8aff2-140">RELATED LINKS</span></span>

[<span data-ttu-id="8aff2-141">Get-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="8aff2-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="8aff2-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="8aff2-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="8aff2-143">Yeni-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="8aff2-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="8aff2-144">Remove-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="8aff2-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="8aff2-145">Set-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="8aff2-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="8aff2-146">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="8aff2-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


