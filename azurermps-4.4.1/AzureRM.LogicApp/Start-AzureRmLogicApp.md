---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: ed8a8c198f626d569d47a9b06b6d9595517f2f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595155"
---
# <span data-ttu-id="ad550-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ad550-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="ad550-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad550-102">SYNOPSIS</span></span>
<span data-ttu-id="ad550-103">Kaynak grubunda bir mantık uygulaması çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="ad550-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad550-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad550-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad550-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad550-105">DESCRIPTION</span></span>
<span data-ttu-id="ad550-106">**Start-Azurermlogicuyg** cmdlet 'ı, mantık uygulamaları özelliğini kullanarak bir mantık uygulaması çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="ad550-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="ad550-107">Bir ad, kaynak grubu ve tetik belirtin.</span><span class="sxs-lookup"><span data-stu-id="ad550-107">Specify a name, resource group, and trigger.</span></span>

<span data-ttu-id="ad550-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="ad550-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ad550-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="ad550-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ad550-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="ad550-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ad550-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="ad550-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ad550-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad550-112">EXAMPLES</span></span>

### <span data-ttu-id="ad550-113">Örnek 1: mantık uygulaması Çalıştır</span><span class="sxs-lookup"><span data-stu-id="ad550-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="ad550-114">Bu komut, ResourceGroup11 adlı kaynak grubundaki mantık uygulamasını çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="ad550-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ad550-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad550-115">PARAMETERS</span></span>

### <span data-ttu-id="ad550-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad550-116">-Name</span></span>
<span data-ttu-id="ad550-117">Bu cmdlet 'in başladığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad550-117">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ad550-118">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="ad550-118">-Parameters</span></span>
<span data-ttu-id="ad550-119">Mantık uygulamasının parametre koleksiyonu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad550-119">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="ad550-120">Karma tablo, sözlük \<string\> veya sözlük belirtin \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="ad550-120">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="ad550-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad550-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad550-122">Bu cmdlet 'in başladığı mantık uygulamasını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad550-122">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ad550-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="ad550-123">-TriggerName</span></span>
<span data-ttu-id="ad550-124">Bu cmdlet 'in başladığı mantık uygulamasının tetikleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad550-124">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ad550-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad550-125">-Confirm</span></span>
<span data-ttu-id="ad550-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad550-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad550-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad550-127">-WhatIf</span></span>
<span data-ttu-id="ad550-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad550-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad550-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad550-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad550-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad550-130">-DefaultProfile</span></span>
<span data-ttu-id="ad550-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad550-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad550-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad550-132">CommonParameters</span></span>
<span data-ttu-id="ad550-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad550-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad550-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad550-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad550-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad550-135">INPUTS</span></span>

## <span data-ttu-id="ad550-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad550-136">OUTPUTS</span></span>

### <span data-ttu-id="ad550-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="ad550-137">System.Object</span></span>

## <span data-ttu-id="ad550-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad550-138">NOTES</span></span>

## <span data-ttu-id="ad550-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad550-139">RELATED LINKS</span></span>

[<span data-ttu-id="ad550-140">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ad550-140">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="ad550-141">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="ad550-141">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="ad550-142">Yeni-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ad550-142">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="ad550-143">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ad550-143">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="ad550-144">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ad550-144">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="ad550-145">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="ad550-145">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


