---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 5f4cfe702b975bf69098aa3c002c756b5cf3da78
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097393"
---
# <span data-ttu-id="735e2-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="735e2-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="735e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="735e2-102">SYNOPSIS</span></span>
<span data-ttu-id="735e2-103">Azure IoT Hub cihaz sağlama hizmetinde paylaşılan erişim ilkelerini silme.</span><span class="sxs-lookup"><span data-stu-id="735e2-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="735e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="735e2-104">SYNTAX</span></span>

### <span data-ttu-id="735e2-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="735e2-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="735e2-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="735e2-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="735e2-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="735e2-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="735e2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="735e2-108">DESCRIPTION</span></span>
<span data-ttu-id="735e2-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="735e2-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="735e2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="735e2-110">EXAMPLES</span></span>

### <span data-ttu-id="735e2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="735e2-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="735e2-112">Azure IoT Hub cihaz sağlama hizmetindeki paylaşılan erişim ilkesini silme "mypolicy".</span><span class="sxs-lookup"><span data-stu-id="735e2-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="735e2-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="735e2-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="735e2-114">Ardışık düzen kullanan bir Azure IoT Hub cihaz sağlama hizmetindeki "mypolicy" paylaşılan erişim ilkesini silme.</span><span class="sxs-lookup"><span data-stu-id="735e2-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="735e2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="735e2-115">PARAMETERS</span></span>

### <span data-ttu-id="735e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735e2-116">-DefaultProfile</span></span>
<span data-ttu-id="735e2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="735e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="735e2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="735e2-118">-InputObject</span></span>
<span data-ttu-id="735e2-119">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="735e2-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="735e2-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="735e2-120">-KeyName</span></span>
<span data-ttu-id="735e2-121">IoT cihazı sağlama hizmeti erişim ilkesi anahtar adı</span><span class="sxs-lookup"><span data-stu-id="735e2-121">IoT Device Provisioning Service access policy key name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735e2-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="735e2-122">-Name</span></span>
<span data-ttu-id="735e2-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="735e2-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="735e2-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="735e2-124">-PassThru</span></span>
<span data-ttu-id="735e2-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="735e2-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735e2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="735e2-126">-ResourceGroupName</span></span>
<span data-ttu-id="735e2-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="735e2-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="735e2-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="735e2-128">-ResourceId</span></span>
<span data-ttu-id="735e2-129">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="735e2-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="735e2-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="735e2-130">-Confirm</span></span>
<span data-ttu-id="735e2-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="735e2-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735e2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="735e2-132">-WhatIf</span></span>
<span data-ttu-id="735e2-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="735e2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="735e2-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="735e2-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735e2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735e2-135">CommonParameters</span></span>
<span data-ttu-id="735e2-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="735e2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735e2-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="735e2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735e2-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="735e2-138">INPUTS</span></span>

### <span data-ttu-id="735e2-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Pssharedaccesstabetureauthorizationruleaccesssıntsdescription</span><span class="sxs-lookup"><span data-stu-id="735e2-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="735e2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="735e2-140">System.String</span></span>

## <span data-ttu-id="735e2-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="735e2-141">OUTPUTS</span></span>

### <span data-ttu-id="735e2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="735e2-142">System.Boolean</span></span>

## <span data-ttu-id="735e2-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="735e2-143">NOTES</span></span>

## <span data-ttu-id="735e2-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="735e2-144">RELATED LINKS</span></span>
