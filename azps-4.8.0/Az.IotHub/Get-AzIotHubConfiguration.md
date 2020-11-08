---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268845"
---
# <span data-ttu-id="56351-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="56351-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="56351-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56351-102">SYNOPSIS</span></span>
<span data-ttu-id="56351-103">Tüm veya belirli bir IoT otomatik cihaz yönetimi yapılandırmasını listeler.</span><span class="sxs-lookup"><span data-stu-id="56351-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="56351-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56351-104">SYNTAX</span></span>

### <span data-ttu-id="56351-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="56351-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56351-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="56351-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56351-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="56351-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56351-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="56351-108">DESCRIPTION</span></span>
<span data-ttu-id="56351-109">IoT Hub 'ındaki bir IoT otomatik cihaz yönetimi yapılandırması veya listesi</span><span class="sxs-lookup"><span data-stu-id="56351-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="56351-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="56351-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="56351-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56351-111">EXAMPLES</span></span>

### <span data-ttu-id="56351-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="56351-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="56351-113">IoT otomatik cihaz yönetimi yapılandırmasının ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="56351-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="56351-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="56351-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="56351-115">IoT Hub 'ındaki IoT otomatik cihaz yönetimi yapılandırmalarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="56351-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="56351-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56351-116">PARAMETERS</span></span>

### <span data-ttu-id="56351-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56351-117">-DefaultProfile</span></span>
<span data-ttu-id="56351-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56351-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56351-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56351-119">-InputObject</span></span>
<span data-ttu-id="56351-120">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="56351-120">IotHub object</span></span>

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

### <span data-ttu-id="56351-121">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="56351-121">-IotHubName</span></span>
<span data-ttu-id="56351-122">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="56351-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="56351-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="56351-123">-Name</span></span>
<span data-ttu-id="56351-124">Yapılandırma kimliği.</span><span class="sxs-lookup"><span data-stu-id="56351-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="56351-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56351-125">-ResourceGroupName</span></span>
<span data-ttu-id="56351-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="56351-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="56351-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="56351-127">-ResourceId</span></span>
<span data-ttu-id="56351-128">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="56351-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="56351-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56351-129">CommonParameters</span></span>
<span data-ttu-id="56351-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56351-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56351-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56351-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56351-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56351-132">INPUTS</span></span>

### <span data-ttu-id="56351-133">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="56351-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="56351-134">System. String</span><span class="sxs-lookup"><span data-stu-id="56351-134">System.String</span></span>

## <span data-ttu-id="56351-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56351-135">OUTPUTS</span></span>

### <span data-ttu-id="56351-136">Microsoft. Azure. Commands. Management. IotHub. modeller. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="56351-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="56351-137">Microsoft. Azure. Commands. Management. IotHub. modeller. PSConfigurations []</span><span class="sxs-lookup"><span data-stu-id="56351-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="56351-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56351-138">NOTES</span></span>

## <span data-ttu-id="56351-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56351-139">RELATED LINKS</span></span>
