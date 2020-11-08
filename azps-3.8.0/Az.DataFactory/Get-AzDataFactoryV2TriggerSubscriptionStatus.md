---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938355"
---
# <span data-ttu-id="2ab88-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="2ab88-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="2ab88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ab88-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab88-103">Olay tetikleyicisi için aboneliğin durumunu belirtilen dış hizmet olaylarına alın.</span><span class="sxs-lookup"><span data-stu-id="2ab88-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="2ab88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ab88-104">SYNTAX</span></span>

### <span data-ttu-id="2ab88-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ab88-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ab88-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2ab88-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ab88-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2ab88-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ab88-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ab88-108">DESCRIPTION</span></span>
<span data-ttu-id="2ab88-109">Bu komut, olay tetikleyicisi için belirtilen dış hizmet olaylarına aboneliğin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="2ab88-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="2ab88-110">Tetik, iade durumu "Enabled" olana kadar başlatılamıyor.</span><span class="sxs-lookup"><span data-stu-id="2ab88-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="2ab88-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ab88-111">EXAMPLES</span></span>

### <span data-ttu-id="2ab88-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ab88-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="2ab88-113">Bu komut, BlobEnetTrigger1 tetikleyicisi için subscribtion 'in durumunu dış hizmet olaylarına alır.</span><span class="sxs-lookup"><span data-stu-id="2ab88-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="2ab88-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ab88-114">PARAMETERS</span></span>

### <span data-ttu-id="2ab88-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2ab88-115">-DataFactoryName</span></span>
<span data-ttu-id="2ab88-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="2ab88-116">The data factory name.</span></span>

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

### <span data-ttu-id="2ab88-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab88-117">-DefaultProfile</span></span>
<span data-ttu-id="2ab88-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ab88-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ab88-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ab88-119">-InputObject</span></span>
<span data-ttu-id="2ab88-120">Tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2ab88-120">The trigger object.</span></span>

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

### <span data-ttu-id="2ab88-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ab88-121">-Name</span></span>
<span data-ttu-id="2ab88-122">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="2ab88-122">The trigger name.</span></span>

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

### <span data-ttu-id="2ab88-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ab88-123">-ResourceGroupName</span></span>
<span data-ttu-id="2ab88-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2ab88-124">The resource group name.</span></span>

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

### <span data-ttu-id="2ab88-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ab88-125">-ResourceId</span></span>
<span data-ttu-id="2ab88-126">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="2ab88-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2ab88-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab88-127">CommonParameters</span></span>
<span data-ttu-id="2ab88-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ab88-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab88-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ab88-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab88-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ab88-130">INPUTS</span></span>

### <span data-ttu-id="2ab88-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2ab88-131">System.String</span></span>
<span data-ttu-id="2ab88-132">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="2ab88-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="2ab88-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ab88-133">OUTPUTS</span></span>

### <span data-ttu-id="2ab88-134">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pçarpıcı Ggersubscriptionstatus</span><span class="sxs-lookup"><span data-stu-id="2ab88-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="2ab88-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ab88-135">NOTES</span></span>

## <span data-ttu-id="2ab88-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ab88-136">RELATED LINKS</span></span>
