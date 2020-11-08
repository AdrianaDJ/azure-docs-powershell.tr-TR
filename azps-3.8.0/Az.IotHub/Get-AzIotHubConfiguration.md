---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095928"
---
# <span data-ttu-id="0a723-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a723-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="0a723-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a723-102">SYNOPSIS</span></span>
<span data-ttu-id="0a723-103">Tüm veya belirli bir IoT otomatik cihaz yönetimi yapılandırmasını listeler.</span><span class="sxs-lookup"><span data-stu-id="0a723-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="0a723-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a723-104">SYNTAX</span></span>

### <span data-ttu-id="0a723-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0a723-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a723-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="0a723-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a723-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="0a723-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a723-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a723-108">DESCRIPTION</span></span>
<span data-ttu-id="0a723-109">IoT Hub 'ındaki bir IoT otomatik cihaz yönetimi yapılandırması veya listesi</span><span class="sxs-lookup"><span data-stu-id="0a723-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="0a723-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="0a723-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="0a723-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a723-111">EXAMPLES</span></span>

### <span data-ttu-id="0a723-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0a723-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="0a723-113">IoT otomatik cihaz yönetimi yapılandırmasının ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="0a723-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="0a723-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0a723-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="0a723-115">IoT Hub 'ındaki IoT otomatik cihaz yönetimi yapılandırmalarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="0a723-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="0a723-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a723-116">PARAMETERS</span></span>

### <span data-ttu-id="0a723-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a723-117">-DefaultProfile</span></span>
<span data-ttu-id="0a723-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a723-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a723-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a723-119">-InputObject</span></span>
<span data-ttu-id="0a723-120">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="0a723-120">IotHub object</span></span>

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

### <span data-ttu-id="0a723-121">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="0a723-121">-IotHubName</span></span>
<span data-ttu-id="0a723-122">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="0a723-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0a723-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="0a723-123">-Name</span></span>
<span data-ttu-id="0a723-124">Yapılandırma kimliği.</span><span class="sxs-lookup"><span data-stu-id="0a723-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="0a723-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a723-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a723-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="0a723-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0a723-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0a723-127">-ResourceId</span></span>
<span data-ttu-id="0a723-128">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0a723-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0a723-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a723-129">CommonParameters</span></span>
<span data-ttu-id="0a723-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a723-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a723-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a723-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a723-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a723-132">INPUTS</span></span>

### <span data-ttu-id="0a723-133">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="0a723-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0a723-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0a723-134">System.String</span></span>

## <span data-ttu-id="0a723-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a723-135">OUTPUTS</span></span>

### <span data-ttu-id="0a723-136">Microsoft. Azure. Commands. Management. IotHub. modeller. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a723-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="0a723-137">Microsoft. Azure. Commands. Management. IotHub. modeller. PSConfigurations []</span><span class="sxs-lookup"><span data-stu-id="0a723-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="0a723-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a723-138">NOTES</span></span>

## <span data-ttu-id="0a723-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a723-139">RELATED LINKS</span></span>
