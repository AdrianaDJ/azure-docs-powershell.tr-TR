---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: b3a813623ed11a64a23dc35afe2f81c3f5de61da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591965"
---
# <span data-ttu-id="4badb-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4badb-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="4badb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4badb-102">SYNOPSIS</span></span>
<span data-ttu-id="4badb-103">Azure IoT Hub cihaz sağlama hizmetinde paylaşılan erişim ilkelerini silme.</span><span class="sxs-lookup"><span data-stu-id="4badb-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4badb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4badb-104">SYNTAX</span></span>

### <span data-ttu-id="4badb-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4badb-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4badb-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="4badb-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4badb-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="4badb-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4badb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4badb-108">DESCRIPTION</span></span>
<span data-ttu-id="4badb-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="4badb-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="4badb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4badb-110">EXAMPLES</span></span>

### <span data-ttu-id="4badb-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4badb-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="4badb-112">Azure IoT Hub cihaz sağlama hizmetindeki paylaşılan erişim ilkesini silme "mypolicy".</span><span class="sxs-lookup"><span data-stu-id="4badb-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="4badb-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4badb-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzureRmIoTDpsAccessPolicy
```

<span data-ttu-id="4badb-114">Ardışık düzen kullanan bir Azure IoT Hub cihaz sağlama hizmetindeki "mypolicy" paylaşılan erişim ilkesini silme.</span><span class="sxs-lookup"><span data-stu-id="4badb-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="4badb-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4badb-115">PARAMETERS</span></span>

### <span data-ttu-id="4badb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4badb-116">-DefaultProfile</span></span>
<span data-ttu-id="4badb-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4badb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4badb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4badb-118">-InputObject</span></span>
<span data-ttu-id="4badb-119">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="4badb-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4badb-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="4badb-120">-KeyName</span></span>
<span data-ttu-id="4badb-121">IoT cihazı sağlama hizmeti erişim ilkesi anahtar adı</span><span class="sxs-lookup"><span data-stu-id="4badb-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="4badb-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4badb-122">-Name</span></span>
<span data-ttu-id="4badb-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="4badb-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4badb-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4badb-124">-PassThru</span></span>
<span data-ttu-id="4badb-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="4badb-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4badb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4badb-126">-ResourceGroupName</span></span>
<span data-ttu-id="4badb-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="4badb-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4badb-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4badb-128">-ResourceId</span></span>
<span data-ttu-id="4badb-129">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4badb-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4badb-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="4badb-130">-Confirm</span></span>
<span data-ttu-id="4badb-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4badb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4badb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4badb-132">-WhatIf</span></span>
<span data-ttu-id="4badb-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4badb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4badb-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4badb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4badb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4badb-135">CommonParameters</span></span>
<span data-ttu-id="4badb-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4badb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4badb-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4badb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4badb-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4badb-138">INPUTS</span></span>

### <span data-ttu-id="4badb-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Pssharedaccesstabetureauthorizationruleaccesssıntsdescription</span><span class="sxs-lookup"><span data-stu-id="4badb-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="4badb-140">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4badb-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4badb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4badb-141">System.String</span></span>

## <span data-ttu-id="4badb-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4badb-142">OUTPUTS</span></span>

### <span data-ttu-id="4badb-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4badb-143">System.Boolean</span></span>

## <span data-ttu-id="4badb-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4badb-144">NOTES</span></span>

## <span data-ttu-id="4badb-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4badb-145">RELATED LINKS</span></span>
