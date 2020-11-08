---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: ce1fe3b50d8198dd9ee1965a3a3ab7a2409e1145
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277477"
---
# <span data-ttu-id="121bd-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="121bd-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="121bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="121bd-102">SYNOPSIS</span></span>
<span data-ttu-id="121bd-103">Cihaz kayıt grubunu silme.</span><span class="sxs-lookup"><span data-stu-id="121bd-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="121bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="121bd-104">SYNTAX</span></span>

### <span data-ttu-id="121bd-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="121bd-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="121bd-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="121bd-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="121bd-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="121bd-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="121bd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="121bd-108">DESCRIPTION</span></span>
<span data-ttu-id="121bd-109">Azure IoT Hub cihaz sağlama hizmetindeki bir kayıt grubunu silme.</span><span class="sxs-lookup"><span data-stu-id="121bd-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="121bd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="121bd-110">EXAMPLES</span></span>

### <span data-ttu-id="121bd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="121bd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="121bd-112">Belirtilen kayıt grubunu silme.</span><span class="sxs-lookup"><span data-stu-id="121bd-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="121bd-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="121bd-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="121bd-114">Tüm kayıt gruplarını silme.</span><span class="sxs-lookup"><span data-stu-id="121bd-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="121bd-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="121bd-115">PARAMETERS</span></span>

### <span data-ttu-id="121bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="121bd-116">-DefaultProfile</span></span>
<span data-ttu-id="121bd-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="121bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="121bd-118">-Vseçpsname</span><span class="sxs-lookup"><span data-stu-id="121bd-118">-DpsName</span></span>
<span data-ttu-id="121bd-119">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="121bd-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="121bd-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="121bd-120">-DpsObject</span></span>
<span data-ttu-id="121bd-121">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="121bd-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="121bd-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="121bd-122">-Name</span></span>
<span data-ttu-id="121bd-123">Kayıt grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="121bd-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="121bd-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="121bd-124">-PassThru</span></span>
<span data-ttu-id="121bd-125">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="121bd-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="121bd-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="121bd-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="121bd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="121bd-127">-ResourceGroupName</span></span>
<span data-ttu-id="121bd-128">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="121bd-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="121bd-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="121bd-129">-ResourceId</span></span>
<span data-ttu-id="121bd-130">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="121bd-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="121bd-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="121bd-131">-Confirm</span></span>
<span data-ttu-id="121bd-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="121bd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="121bd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="121bd-133">-WhatIf</span></span>
<span data-ttu-id="121bd-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="121bd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="121bd-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="121bd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="121bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="121bd-136">CommonParameters</span></span>
<span data-ttu-id="121bd-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="121bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="121bd-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="121bd-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="121bd-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="121bd-139">INPUTS</span></span>

### <span data-ttu-id="121bd-140">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="121bd-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="121bd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="121bd-141">System.String</span></span>

## <span data-ttu-id="121bd-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="121bd-142">OUTPUTS</span></span>

### <span data-ttu-id="121bd-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="121bd-143">System.Boolean</span></span>

## <span data-ttu-id="121bd-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="121bd-144">NOTES</span></span>

## <span data-ttu-id="121bd-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="121bd-145">RELATED LINKS</span></span>
