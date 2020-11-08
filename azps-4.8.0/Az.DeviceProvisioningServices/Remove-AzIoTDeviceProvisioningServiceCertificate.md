---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274997"
---
# <span data-ttu-id="48190-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="48190-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="48190-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48190-102">SYNOPSIS</span></span>
<span data-ttu-id="48190-103">Azure IoT Hub cihaz sağlama hizmeti sertifikasını silme.</span><span class="sxs-lookup"><span data-stu-id="48190-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="48190-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48190-104">SYNTAX</span></span>

### <span data-ttu-id="48190-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="48190-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48190-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="48190-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48190-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="48190-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48190-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="48190-108">DESCRIPTION</span></span>
<span data-ttu-id="48190-109">Azure IoT Hub cihaz hazırlama hizmetindeki CA sertifikalarının ayrıntılı açıklaması için bkz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="48190-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="48190-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48190-110">EXAMPLES</span></span>

### <span data-ttu-id="48190-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="48190-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="48190-112">Bir Azure IoT Hub cihaz sağlama hizmetinde "sertifikasertifikası" öğesini silin.</span><span class="sxs-lookup"><span data-stu-id="48190-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="48190-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48190-113">PARAMETERS</span></span>

### <span data-ttu-id="48190-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="48190-114">-CertificateName</span></span>
<span data-ttu-id="48190-115">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="48190-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="48190-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48190-116">-DefaultProfile</span></span>
<span data-ttu-id="48190-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48190-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48190-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="48190-118">-Etag</span></span>
<span data-ttu-id="48190-119">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="48190-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="48190-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48190-120">-InputObject</span></span>
<span data-ttu-id="48190-121">IoT cihaz sağlama hizmeti sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="48190-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="48190-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="48190-122">-Name</span></span>
<span data-ttu-id="48190-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="48190-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="48190-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="48190-124">-PassThru</span></span>
<span data-ttu-id="48190-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="48190-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="48190-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48190-126">-ResourceGroupName</span></span>
<span data-ttu-id="48190-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="48190-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="48190-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="48190-128">-ResourceId</span></span>
<span data-ttu-id="48190-129">IoT cihaz sağlama hizmeti sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="48190-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="48190-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="48190-130">-Confirm</span></span>
<span data-ttu-id="48190-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="48190-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48190-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48190-132">-WhatIf</span></span>
<span data-ttu-id="48190-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="48190-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48190-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="48190-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48190-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48190-135">CommonParameters</span></span>
<span data-ttu-id="48190-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48190-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48190-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48190-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48190-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48190-138">INPUTS</span></span>

### <span data-ttu-id="48190-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="48190-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="48190-140">System. String</span><span class="sxs-lookup"><span data-stu-id="48190-140">System.String</span></span>

## <span data-ttu-id="48190-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48190-141">OUTPUTS</span></span>

### <span data-ttu-id="48190-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48190-142">System.Boolean</span></span>

## <span data-ttu-id="48190-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48190-143">NOTES</span></span>

## <span data-ttu-id="48190-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48190-144">RELATED LINKS</span></span>
