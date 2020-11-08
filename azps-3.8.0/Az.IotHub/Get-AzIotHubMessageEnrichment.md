---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096303"
---
# <span data-ttu-id="169ea-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="169ea-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="169ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="169ea-102">SYNOPSIS</span></span>
<span data-ttu-id="169ea-103">Tüm ileti zenginleştirme veya IoT merkeziniz için belirli bir ileti zenginleştirme.</span><span class="sxs-lookup"><span data-stu-id="169ea-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="169ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="169ea-104">SYNTAX</span></span>

### <span data-ttu-id="169ea-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="169ea-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="169ea-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="169ea-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="169ea-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="169ea-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="169ea-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="169ea-108">DESCRIPTION</span></span>
<span data-ttu-id="169ea-109">Azure IoT Hub 'ındaki ileti zenginleştirme hakkında ayrıntılı bir açıklama için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="169ea-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="169ea-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="169ea-110">EXAMPLES</span></span>

### <span data-ttu-id="169ea-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="169ea-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="169ea-112">Tüm ileti zenginleştirme MyIotHub</span><span class="sxs-lookup"><span data-stu-id="169ea-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="169ea-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="169ea-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="169ea-114">"Yenianahtar" ileti zenginleştirme hakkındaki ayrıntıları gösterin.</span><span class="sxs-lookup"><span data-stu-id="169ea-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="169ea-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="169ea-115">PARAMETERS</span></span>

### <span data-ttu-id="169ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="169ea-116">-DefaultProfile</span></span>
<span data-ttu-id="169ea-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="169ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="169ea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="169ea-118">-InputObject</span></span>
<span data-ttu-id="169ea-119">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="169ea-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="169ea-120">-Tuşlu</span><span class="sxs-lookup"><span data-stu-id="169ea-120">-Key</span></span>
<span data-ttu-id="169ea-121">Zenginleştirme tuşu.</span><span class="sxs-lookup"><span data-stu-id="169ea-121">The enrichment's key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169ea-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="169ea-122">-Name</span></span>
<span data-ttu-id="169ea-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="169ea-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169ea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="169ea-124">-ResourceGroupName</span></span>
<span data-ttu-id="169ea-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="169ea-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169ea-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="169ea-126">-ResourceId</span></span>
<span data-ttu-id="169ea-127">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="169ea-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169ea-128">CommonParameters</span></span>
<span data-ttu-id="169ea-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="169ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169ea-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="169ea-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169ea-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="169ea-131">INPUTS</span></span>

### <span data-ttu-id="169ea-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="169ea-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="169ea-133">System. String</span><span class="sxs-lookup"><span data-stu-id="169ea-133">System.String</span></span>

## <span data-ttu-id="169ea-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="169ea-134">OUTPUTS</span></span>

### <span data-ttu-id="169ea-135">Microsoft. Azure. Commands. Management. IotHub. modeller. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="169ea-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="169ea-136">Microsoft. Azure. Commands. Management. IotHub. modeller. PSEnrichmentProperties []</span><span class="sxs-lookup"><span data-stu-id="169ea-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="169ea-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="169ea-137">NOTES</span></span>

## <span data-ttu-id="169ea-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="169ea-138">RELATED LINKS</span></span>