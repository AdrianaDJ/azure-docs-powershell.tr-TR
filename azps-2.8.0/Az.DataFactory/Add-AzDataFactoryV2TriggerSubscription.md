---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c99626e1323f10e98dcef1efc7ae622aab5f6b5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752570"
---
# <span data-ttu-id="510a1-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="510a1-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="510a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="510a1-102">SYNOPSIS</span></span>
<span data-ttu-id="510a1-103">Olay tetikleyicisini dış hizmet olaylarına abone olun.</span><span class="sxs-lookup"><span data-stu-id="510a1-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="510a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="510a1-104">SYNTAX</span></span>

### <span data-ttu-id="510a1-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="510a1-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="510a1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="510a1-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="510a1-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="510a1-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="510a1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="510a1-108">DESCRIPTION</span></span>
<span data-ttu-id="510a1-109">Bu komut, tetik tanımı 'ndan olay tetikleyicisini belirtilen dış hizmet olaylarına abone olur.</span><span class="sxs-lookup"><span data-stu-id="510a1-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="510a1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="510a1-110">EXAMPLES</span></span>

### <span data-ttu-id="510a1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="510a1-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="510a1-112">Bu komut, tetik tanımı 'ndan belirtilen olaylarda BlobEnetTrigger1 tetikleyicisini abone olur.</span><span class="sxs-lookup"><span data-stu-id="510a1-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="510a1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="510a1-113">PARAMETERS</span></span>

### <span data-ttu-id="510a1-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="510a1-114">-DataFactoryName</span></span>
<span data-ttu-id="510a1-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="510a1-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="510a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="510a1-116">-DefaultProfile</span></span>
<span data-ttu-id="510a1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="510a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510a1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="510a1-118">-InputObject</span></span>
<span data-ttu-id="510a1-119">Tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="510a1-119">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="510a1-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="510a1-120">-Name</span></span>
<span data-ttu-id="510a1-121">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="510a1-121">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="510a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="510a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="510a1-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="510a1-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="510a1-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="510a1-124">-ResourceId</span></span>
<span data-ttu-id="510a1-125">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="510a1-125">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="510a1-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="510a1-126">-Confirm</span></span>
<span data-ttu-id="510a1-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="510a1-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510a1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="510a1-128">-WhatIf</span></span>
<span data-ttu-id="510a1-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="510a1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="510a1-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="510a1-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="510a1-131">CommonParameters</span></span>
<span data-ttu-id="510a1-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="510a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="510a1-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="510a1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="510a1-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="510a1-134">INPUTS</span></span>

### <span data-ttu-id="510a1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="510a1-135">System.String</span></span>
<span data-ttu-id="510a1-136">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="510a1-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="510a1-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="510a1-137">OUTPUTS</span></span>

### <span data-ttu-id="510a1-138">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pçarpıcı Ggersubscriptionstatus</span><span class="sxs-lookup"><span data-stu-id="510a1-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="510a1-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="510a1-139">NOTES</span></span>

## <span data-ttu-id="510a1-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="510a1-140">RELATED LINKS</span></span>

