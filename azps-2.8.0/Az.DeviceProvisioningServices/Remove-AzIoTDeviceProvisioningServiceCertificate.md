---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: e03bb9f8f996c274abe07dd3e1b005760756d632
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752055"
---
# <span data-ttu-id="9c6bf-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="9c6bf-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="9c6bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="9c6bf-103">Azure IoT Hub cihaz sağlama hizmeti sertifikasını silme.</span><span class="sxs-lookup"><span data-stu-id="9c6bf-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="9c6bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c6bf-104">SYNTAX</span></span>

### <span data-ttu-id="9c6bf-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9c6bf-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c6bf-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="9c6bf-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c6bf-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="9c6bf-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c6bf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c6bf-108">DESCRIPTION</span></span>
<span data-ttu-id="9c6bf-109">Azure IoT Hub cihaz hazırlama hizmetindeki CA sertifikalarının ayrıntılı açıklaması için bkz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="9c6bf-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="9c6bf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c6bf-110">EXAMPLES</span></span>

### <span data-ttu-id="9c6bf-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9c6bf-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="9c6bf-112">Bir Azure IoT Hub cihaz sağlama hizmetinde "sertifikasertifikası" öğesini silin.</span><span class="sxs-lookup"><span data-stu-id="9c6bf-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="9c6bf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c6bf-113">PARAMETERS</span></span>

### <span data-ttu-id="9c6bf-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9c6bf-114">-CertificateName</span></span>
<span data-ttu-id="9c6bf-115">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="9c6bf-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="9c6bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c6bf-116">-DefaultProfile</span></span>
<span data-ttu-id="9c6bf-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c6bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c6bf-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="9c6bf-118">-Etag</span></span>
<span data-ttu-id="9c6bf-119">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="9c6bf-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="9c6bf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c6bf-120">-InputObject</span></span>
<span data-ttu-id="9c6bf-121">IoT cihaz sağlama hizmeti sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="9c6bf-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="9c6bf-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="9c6bf-122">-Name</span></span>
<span data-ttu-id="9c6bf-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="9c6bf-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9c6bf-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9c6bf-124">-PassThru</span></span>
<span data-ttu-id="9c6bf-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="9c6bf-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9c6bf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c6bf-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c6bf-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="9c6bf-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9c6bf-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9c6bf-128">-ResourceId</span></span>
<span data-ttu-id="9c6bf-129">IoT cihaz sağlama hizmeti sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9c6bf-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="9c6bf-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="9c6bf-130">-Confirm</span></span>
<span data-ttu-id="9c6bf-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9c6bf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c6bf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c6bf-132">-WhatIf</span></span>
<span data-ttu-id="9c6bf-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c6bf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c6bf-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9c6bf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c6bf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c6bf-135">CommonParameters</span></span>
<span data-ttu-id="9c6bf-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c6bf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c6bf-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c6bf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c6bf-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c6bf-138">INPUTS</span></span>

### <span data-ttu-id="9c6bf-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="9c6bf-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="9c6bf-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9c6bf-140">System.String</span></span>

## <span data-ttu-id="9c6bf-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c6bf-141">OUTPUTS</span></span>

### <span data-ttu-id="9c6bf-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c6bf-142">System.Boolean</span></span>

## <span data-ttu-id="9c6bf-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c6bf-143">NOTES</span></span>

## <span data-ttu-id="9c6bf-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c6bf-144">RELATED LINKS</span></span>
