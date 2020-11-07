---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/start-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: fefe9da2d0339c22d0f41e1526d8664ff27a52d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764993"
---
# <span data-ttu-id="45e59-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="45e59-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="45e59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45e59-102">SYNOPSIS</span></span>
<span data-ttu-id="45e59-103">Kaynak grubunda bir mantık uygulaması çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="45e59-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45e59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45e59-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45e59-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45e59-105">DESCRIPTION</span></span>
<span data-ttu-id="45e59-106">**Start-Azurermlogicuyg** cmdlet 'ı, mantık uygulamaları özelliğini kullanarak bir mantık uygulaması çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="45e59-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="45e59-107">Bir ad, kaynak grubu ve tetik belirtin.</span><span class="sxs-lookup"><span data-stu-id="45e59-107">Specify a name, resource group, and trigger.</span></span>

<span data-ttu-id="45e59-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="45e59-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="45e59-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="45e59-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="45e59-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="45e59-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="45e59-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="45e59-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="45e59-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45e59-112">EXAMPLES</span></span>

### <span data-ttu-id="45e59-113">Örnek 1: mantık uygulaması Çalıştır</span><span class="sxs-lookup"><span data-stu-id="45e59-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="45e59-114">Bu komut, ResourceGroup11 adlı kaynak grubundaki mantık uygulamasını çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="45e59-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="45e59-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45e59-115">PARAMETERS</span></span>

### <span data-ttu-id="45e59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e59-116">-DefaultProfile</span></span>
<span data-ttu-id="45e59-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="45e59-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e59-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="45e59-118">-Name</span></span>
<span data-ttu-id="45e59-119">Bu cmdlet 'in başladığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45e59-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45e59-120">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="45e59-120">-Parameters</span></span>
<span data-ttu-id="45e59-121">Mantık uygulamasının parametre koleksiyonu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="45e59-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="45e59-122">Karma tablo, sözlük \<string\> veya sözlük belirtin \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="45e59-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e59-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45e59-123">-ResourceGroupName</span></span>
<span data-ttu-id="45e59-124">Bu cmdlet 'in başladığı mantık uygulamasını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45e59-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45e59-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="45e59-125">-TriggerName</span></span>
<span data-ttu-id="45e59-126">Bu cmdlet 'in başladığı mantık uygulamasının tetikleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45e59-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45e59-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="45e59-127">-Confirm</span></span>
<span data-ttu-id="45e59-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="45e59-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e59-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45e59-129">-WhatIf</span></span>
<span data-ttu-id="45e59-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="45e59-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45e59-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="45e59-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e59-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e59-132">CommonParameters</span></span>
<span data-ttu-id="45e59-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45e59-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e59-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45e59-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e59-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45e59-135">INPUTS</span></span>

### <span data-ttu-id="45e59-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="45e59-136">None</span></span>
<span data-ttu-id="45e59-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="45e59-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45e59-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45e59-138">OUTPUTS</span></span>

### <span data-ttu-id="45e59-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="45e59-139">System.Object</span></span>

## <span data-ttu-id="45e59-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45e59-140">NOTES</span></span>

## <span data-ttu-id="45e59-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45e59-141">RELATED LINKS</span></span>

[<span data-ttu-id="45e59-142">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="45e59-142">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="45e59-143">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="45e59-143">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="45e59-144">Yeni-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="45e59-144">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="45e59-145">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="45e59-145">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="45e59-146">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="45e59-146">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="45e59-147">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="45e59-147">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


