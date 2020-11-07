---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 7d41a75473d26b113e5d4e4163775269b8b9f60d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760906"
---
# <span data-ttu-id="48296-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="48296-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="48296-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48296-102">SYNOPSIS</span></span>
<span data-ttu-id="48296-103">Azure IoT Hub cihazı sağlama hizmetini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="48296-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="48296-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48296-104">SYNTAX</span></span>

### <span data-ttu-id="48296-105">ResourceUpdateSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="48296-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48296-106">Inputobjectupdateset</span><span class="sxs-lookup"><span data-stu-id="48296-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48296-107">Inputobjectcreateupdateset</span><span class="sxs-lookup"><span data-stu-id="48296-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48296-108">Resourceıdupdateset</span><span class="sxs-lookup"><span data-stu-id="48296-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48296-109">Resourceıdcreateupdateset</span><span class="sxs-lookup"><span data-stu-id="48296-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48296-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="48296-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48296-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="48296-111">DESCRIPTION</span></span>
<span data-ttu-id="48296-112">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="48296-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="48296-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48296-113">EXAMPLES</span></span>

### <span data-ttu-id="48296-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="48296-114">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : GeoLatency
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="48296-115">"Myıotdps" Azure IoT Hub cihaz sağlama hizmetinden "bir</span><span class="sxs-lookup"><span data-stu-id="48296-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="48296-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="48296-116">Example 2</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="48296-117">" @tags " Öğesini Azure IoT Hub cihaz sağlama hizmetinin "myıotdps" etiketine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="48296-117">Add "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="48296-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="48296-118">Example 3</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag @tags -Reset

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAS1dY=
```

<span data-ttu-id="48296-119">@tagsArdışık düzen kullanan "myıotdps" adlı Azure IoT Hub cihaz sağlama hizmeti etiketine ve yeni "" etiketini silin.</span><span class="sxs-lookup"><span data-stu-id="48296-119">Delete Tag and add new "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="48296-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48296-120">PARAMETERS</span></span>

### <span data-ttu-id="48296-121">-Ayıra Ilkesi</span><span class="sxs-lookup"><span data-stu-id="48296-121">-AllocationPolicy</span></span>
<span data-ttu-id="48296-122">IoT cihaz sağlama hizmeti ayırma ilkesi</span><span class="sxs-lookup"><span data-stu-id="48296-122">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectCreateUpdateSet, ResourceIdCreateUpdateSet, ResourceCreateUpdateSet
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48296-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48296-123">-DefaultProfile</span></span>
<span data-ttu-id="48296-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48296-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48296-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48296-125">-InputObject</span></span>
<span data-ttu-id="48296-126">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="48296-126">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectUpdateSet, InputObjectCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48296-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="48296-127">-Name</span></span>
<span data-ttu-id="48296-128">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="48296-128">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48296-129">-Reset</span><span class="sxs-lookup"><span data-stu-id="48296-129">-Reset</span></span>
<span data-ttu-id="48296-130">IoT cihaz sağlama hizmeti etiketlerini sıfırlama</span><span class="sxs-lookup"><span data-stu-id="48296-130">Reset IoT Device Provisioning Service Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48296-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48296-131">-ResourceGroupName</span></span>
<span data-ttu-id="48296-132">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="48296-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48296-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="48296-133">-ResourceId</span></span>
<span data-ttu-id="48296-134">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="48296-134">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdUpdateSet, ResourceIdCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48296-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="48296-135">-Tag</span></span>
<span data-ttu-id="48296-136">IoT cihazı sağlama hizmeti etiket koleksiyonu</span><span class="sxs-lookup"><span data-stu-id="48296-136">IoT Device Provisioning Service Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48296-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="48296-137">-Confirm</span></span>
<span data-ttu-id="48296-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="48296-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48296-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48296-139">-WhatIf</span></span>
<span data-ttu-id="48296-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="48296-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48296-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="48296-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48296-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48296-142">CommonParameters</span></span>
<span data-ttu-id="48296-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48296-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48296-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48296-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48296-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48296-145">INPUTS</span></span>

### <span data-ttu-id="48296-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="48296-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="48296-147">System. String</span><span class="sxs-lookup"><span data-stu-id="48296-147">System.String</span></span>

## <span data-ttu-id="48296-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48296-148">OUTPUTS</span></span>

### <span data-ttu-id="48296-149">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="48296-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="48296-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48296-150">NOTES</span></span>

## <span data-ttu-id="48296-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48296-151">RELATED LINKS</span></span>