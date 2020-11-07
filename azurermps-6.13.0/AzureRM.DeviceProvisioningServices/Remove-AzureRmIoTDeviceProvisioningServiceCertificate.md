---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 64de44e74b5c6ea21d9d49b1911bcd34a74a374a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762946"
---
# <span data-ttu-id="c4c02-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="c4c02-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="c4c02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4c02-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c02-103">Azure IoT Hub cihaz sağlama hizmeti sertifikasını silme.</span><span class="sxs-lookup"><span data-stu-id="c4c02-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4c02-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4c02-104">SYNTAX</span></span>

### <span data-ttu-id="c4c02-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c4c02-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4c02-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="c4c02-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4c02-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="c4c02-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4c02-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4c02-108">DESCRIPTION</span></span>
<span data-ttu-id="c4c02-109">Azure IoT Hub cihaz hazırlama hizmetindeki CA sertifikalarının ayrıntılı açıklaması için bkz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="c4c02-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="c4c02-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4c02-110">EXAMPLES</span></span>

### <span data-ttu-id="c4c02-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c4c02-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="c4c02-112">Bir Azure IoT Hub cihaz sağlama hizmetinde "sertifikasertifikası" öğesini silin.</span><span class="sxs-lookup"><span data-stu-id="c4c02-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c4c02-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4c02-113">PARAMETERS</span></span>

### <span data-ttu-id="c4c02-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c4c02-114">-CertificateName</span></span>
<span data-ttu-id="c4c02-115">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="c4c02-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c02-116">-DefaultProfile</span></span>
<span data-ttu-id="c4c02-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c4c02-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4c02-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="c4c02-118">-Etag</span></span>
<span data-ttu-id="c4c02-119">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="c4c02-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="c4c02-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4c02-120">-InputObject</span></span>
<span data-ttu-id="c4c02-121">IoT cihaz sağlama hizmeti sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="c4c02-121">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c02-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c4c02-122">-Name</span></span>
<span data-ttu-id="c4c02-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="c4c02-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c4c02-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c4c02-124">-PassThru</span></span>
<span data-ttu-id="c4c02-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="c4c02-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c4c02-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4c02-126">-ResourceGroupName</span></span>
<span data-ttu-id="c4c02-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="c4c02-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c4c02-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c4c02-128">-ResourceId</span></span>
<span data-ttu-id="c4c02-129">IoT cihaz sağlama hizmeti sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c4c02-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="c4c02-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="c4c02-130">-Confirm</span></span>
<span data-ttu-id="c4c02-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4c02-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4c02-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4c02-132">-WhatIf</span></span>
<span data-ttu-id="c4c02-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4c02-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4c02-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c4c02-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4c02-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c02-135">CommonParameters</span></span>
<span data-ttu-id="c4c02-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4c02-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c02-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4c02-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c02-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4c02-138">INPUTS</span></span>

### <span data-ttu-id="c4c02-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="c4c02-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="c4c02-140">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c4c02-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c4c02-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c4c02-141">System.String</span></span>

## <span data-ttu-id="c4c02-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4c02-142">OUTPUTS</span></span>

### <span data-ttu-id="c4c02-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4c02-143">System.Boolean</span></span>

## <span data-ttu-id="c4c02-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4c02-144">NOTES</span></span>

## <span data-ttu-id="c4c02-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4c02-145">RELATED LINKS</span></span>
