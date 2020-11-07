---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 6c47e2de9a234d5ae52598002d2ec5db93748692
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751749"
---
# <span data-ttu-id="433b9-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="433b9-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="433b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="433b9-102">SYNOPSIS</span></span>
<span data-ttu-id="433b9-103">Tüm ileti zenginleştirme veya IoT merkeziniz için belirli bir ileti zenginleştirme.</span><span class="sxs-lookup"><span data-stu-id="433b9-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="433b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="433b9-104">SYNTAX</span></span>

### <span data-ttu-id="433b9-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="433b9-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="433b9-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="433b9-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="433b9-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="433b9-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="433b9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="433b9-108">DESCRIPTION</span></span>
<span data-ttu-id="433b9-109">Azure IoT Hub 'ındaki ileti zenginleştirme hakkında ayrıntılı bir açıklama için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="433b9-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="433b9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="433b9-110">EXAMPLES</span></span>

### <span data-ttu-id="433b9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="433b9-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="433b9-112">Tüm ileti zenginleştirme MyIotHub</span><span class="sxs-lookup"><span data-stu-id="433b9-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="433b9-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="433b9-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="433b9-114">"Yenianahtar" ileti zenginleştirme hakkındaki ayrıntıları gösterin.</span><span class="sxs-lookup"><span data-stu-id="433b9-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="433b9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="433b9-115">PARAMETERS</span></span>

### <span data-ttu-id="433b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="433b9-116">-DefaultProfile</span></span>
<span data-ttu-id="433b9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="433b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="433b9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="433b9-118">-InputObject</span></span>
<span data-ttu-id="433b9-119">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="433b9-119">IotHub object</span></span>

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

### <span data-ttu-id="433b9-120">-Tuşlu</span><span class="sxs-lookup"><span data-stu-id="433b9-120">-Key</span></span>
<span data-ttu-id="433b9-121">Zenginleştirme tuşu.</span><span class="sxs-lookup"><span data-stu-id="433b9-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="433b9-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="433b9-122">-Name</span></span>
<span data-ttu-id="433b9-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="433b9-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="433b9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="433b9-124">-ResourceGroupName</span></span>
<span data-ttu-id="433b9-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="433b9-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="433b9-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="433b9-126">-ResourceId</span></span>
<span data-ttu-id="433b9-127">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="433b9-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="433b9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433b9-128">CommonParameters</span></span>
<span data-ttu-id="433b9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="433b9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433b9-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="433b9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433b9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="433b9-131">INPUTS</span></span>

### <span data-ttu-id="433b9-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="433b9-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="433b9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="433b9-133">System.String</span></span>

## <span data-ttu-id="433b9-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="433b9-134">OUTPUTS</span></span>

### <span data-ttu-id="433b9-135">Microsoft. Azure. Commands. Management. IotHub. modeller. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="433b9-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="433b9-136">Microsoft. Azure. Commands. Management. IotHub. modeller. PSEnrichmentProperties []</span><span class="sxs-lookup"><span data-stu-id="433b9-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="433b9-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="433b9-137">NOTES</span></span>

## <span data-ttu-id="433b9-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="433b9-138">RELATED LINKS</span></span>
