---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c1e7fab8eb4e8afe22bdebc5930c8599c2dadceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752463"
---
# <span data-ttu-id="674e0-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="674e0-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="674e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="674e0-102">SYNOPSIS</span></span>
<span data-ttu-id="674e0-103">Olay tetikleyicisini dış hizmet olaylarına aboneliğini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="674e0-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="674e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="674e0-104">SYNTAX</span></span>

### <span data-ttu-id="674e0-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="674e0-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="674e0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="674e0-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="674e0-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="674e0-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="674e0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="674e0-108">DESCRIPTION</span></span>
<span data-ttu-id="674e0-109">Bu komut, tetik tanımı 'ndan olay tetikleyicisini belirtilen dış hizmet olaylarına abone olmaz.</span><span class="sxs-lookup"><span data-stu-id="674e0-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="674e0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="674e0-110">EXAMPLES</span></span>

### <span data-ttu-id="674e0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="674e0-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="674e0-112">Bu komut, tetik definteden belirtilen olaylarla BlobEnetTrigger1 tetikleyicisini aboneliğini iptal edecektir.</span><span class="sxs-lookup"><span data-stu-id="674e0-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="674e0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="674e0-113">PARAMETERS</span></span>

### <span data-ttu-id="674e0-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="674e0-114">-DataFactoryName</span></span>
<span data-ttu-id="674e0-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="674e0-115">The data factory name.</span></span>

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

### <span data-ttu-id="674e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="674e0-116">-DefaultProfile</span></span>
<span data-ttu-id="674e0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="674e0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="674e0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="674e0-118">-Force</span></span>
<span data-ttu-id="674e0-119">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="674e0-119">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674e0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="674e0-120">-InputObject</span></span>
<span data-ttu-id="674e0-121">Tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="674e0-121">The trigger object.</span></span>

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

### <span data-ttu-id="674e0-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="674e0-122">-Name</span></span>
<span data-ttu-id="674e0-123">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="674e0-123">The trigger name.</span></span>

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

### <span data-ttu-id="674e0-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="674e0-124">-PassThru</span></span>
<span data-ttu-id="674e0-125">Belirtilmişse, cmdlet başarılı silme durumunda doğru dönüş döndürür.</span><span class="sxs-lookup"><span data-stu-id="674e0-125">If specified, cmdlet will return return true on successful delete.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674e0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="674e0-126">-ResourceGroupName</span></span>
<span data-ttu-id="674e0-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="674e0-127">The resource group name.</span></span>

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

### <span data-ttu-id="674e0-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="674e0-128">-ResourceId</span></span>
<span data-ttu-id="674e0-129">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="674e0-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="674e0-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="674e0-130">-Confirm</span></span>
<span data-ttu-id="674e0-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="674e0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="674e0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="674e0-132">-WhatIf</span></span>
<span data-ttu-id="674e0-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="674e0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="674e0-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="674e0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="674e0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="674e0-135">CommonParameters</span></span>
<span data-ttu-id="674e0-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="674e0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="674e0-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="674e0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="674e0-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="674e0-138">INPUTS</span></span>

### <span data-ttu-id="674e0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="674e0-139">System.String</span></span>
<span data-ttu-id="674e0-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="674e0-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="674e0-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="674e0-141">OUTPUTS</span></span>

### <span data-ttu-id="674e0-142">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pçarpıcı Ggersubscriptionstatus</span><span class="sxs-lookup"><span data-stu-id="674e0-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="674e0-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="674e0-143">NOTES</span></span>

## <span data-ttu-id="674e0-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="674e0-144">RELATED LINKS</span></span>

