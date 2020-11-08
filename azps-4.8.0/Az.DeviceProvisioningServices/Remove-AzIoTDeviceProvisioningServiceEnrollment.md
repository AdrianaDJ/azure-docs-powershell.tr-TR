---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8b16d95d582e29be6f49cac9eaeb00bcda67de0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273609"
---
# <span data-ttu-id="a014f-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="a014f-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="a014f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a014f-102">SYNOPSIS</span></span>
<span data-ttu-id="a014f-103">Bir cihaz kayıt kaydını silme.</span><span class="sxs-lookup"><span data-stu-id="a014f-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="a014f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a014f-104">SYNTAX</span></span>

### <span data-ttu-id="a014f-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a014f-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a014f-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="a014f-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a014f-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="a014f-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a014f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a014f-108">DESCRIPTION</span></span>
<span data-ttu-id="a014f-109">Bir Azure IoT Hub cihaz sağlama hizmetinde bir cihaz kaydını silme.</span><span class="sxs-lookup"><span data-stu-id="a014f-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="a014f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a014f-110">EXAMPLES</span></span>

### <span data-ttu-id="a014f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a014f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="a014f-112">Belirtilen kayıt kaydını silme.</span><span class="sxs-lookup"><span data-stu-id="a014f-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="a014f-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a014f-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="a014f-114">Tüm kayıt kayıtlarını silin.</span><span class="sxs-lookup"><span data-stu-id="a014f-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="a014f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a014f-115">PARAMETERS</span></span>

### <span data-ttu-id="a014f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a014f-116">-DefaultProfile</span></span>
<span data-ttu-id="a014f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a014f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a014f-118">-Vseçpsname</span><span class="sxs-lookup"><span data-stu-id="a014f-118">-DpsName</span></span>
<span data-ttu-id="a014f-119">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="a014f-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a014f-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="a014f-120">-DpsObject</span></span>
<span data-ttu-id="a014f-121">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="a014f-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a014f-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a014f-122">-PassThru</span></span>
<span data-ttu-id="a014f-123">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="a014f-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="a014f-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a014f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a014f-125">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="a014f-125">-RegistrationId</span></span>
<span data-ttu-id="a014f-126">Tek kayıt kayıt kimliği.</span><span class="sxs-lookup"><span data-stu-id="a014f-126">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="a014f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a014f-127">-ResourceGroupName</span></span>
<span data-ttu-id="a014f-128">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a014f-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a014f-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a014f-129">-ResourceId</span></span>
<span data-ttu-id="a014f-130">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a014f-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a014f-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="a014f-131">-Confirm</span></span>
<span data-ttu-id="a014f-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a014f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a014f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a014f-133">-WhatIf</span></span>
<span data-ttu-id="a014f-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a014f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a014f-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a014f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a014f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a014f-136">CommonParameters</span></span>
<span data-ttu-id="a014f-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a014f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a014f-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a014f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a014f-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a014f-139">INPUTS</span></span>

### <span data-ttu-id="a014f-140">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a014f-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="a014f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a014f-141">System.String</span></span>

## <span data-ttu-id="a014f-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a014f-142">OUTPUTS</span></span>

### <span data-ttu-id="a014f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a014f-143">System.Boolean</span></span>

## <span data-ttu-id="a014f-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a014f-144">NOTES</span></span>

## <span data-ttu-id="a014f-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a014f-145">RELATED LINKS</span></span>
