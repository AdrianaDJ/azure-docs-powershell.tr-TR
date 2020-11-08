---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 3e30b7aa3d1e43844fc1fe53e860ee8b8c66f385
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275336"
---
# <span data-ttu-id="52efa-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="52efa-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="52efa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52efa-102">SYNOPSIS</span></span>
<span data-ttu-id="52efa-103">Azure IoT Hub sertifikasını siler.</span><span class="sxs-lookup"><span data-stu-id="52efa-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="52efa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52efa-104">SYNTAX</span></span>

### <span data-ttu-id="52efa-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52efa-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52efa-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="52efa-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52efa-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="52efa-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52efa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="52efa-108">DESCRIPTION</span></span>
<span data-ttu-id="52efa-109">Azure IoT Hub 'daki CA sertifikalarının ayrıntılı açıklaması için bkz: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="52efa-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="52efa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52efa-110">EXAMPLES</span></span>

### <span data-ttu-id="52efa-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="52efa-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="52efa-112">Sertifikamı silme</span><span class="sxs-lookup"><span data-stu-id="52efa-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="52efa-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52efa-113">PARAMETERS</span></span>

### <span data-ttu-id="52efa-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="52efa-114">-CertificateName</span></span>
<span data-ttu-id="52efa-115">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="52efa-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="52efa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52efa-116">-DefaultProfile</span></span>
<span data-ttu-id="52efa-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52efa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52efa-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="52efa-118">-Etag</span></span>
<span data-ttu-id="52efa-119">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="52efa-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="52efa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52efa-120">-InputObject</span></span>
<span data-ttu-id="52efa-121">Sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="52efa-121">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="52efa-122">-Name</span></span>
<span data-ttu-id="52efa-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="52efa-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="52efa-124">-PassThru</span></span>
<span data-ttu-id="52efa-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="52efa-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="52efa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52efa-126">-ResourceGroupName</span></span>
<span data-ttu-id="52efa-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="52efa-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="52efa-128">-ResourceId</span></span>
<span data-ttu-id="52efa-129">Sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="52efa-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="52efa-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="52efa-130">-Confirm</span></span>
<span data-ttu-id="52efa-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="52efa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52efa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52efa-132">-WhatIf</span></span>
<span data-ttu-id="52efa-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52efa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52efa-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="52efa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52efa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52efa-135">CommonParameters</span></span>
<span data-ttu-id="52efa-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52efa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52efa-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52efa-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52efa-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52efa-138">INPUTS</span></span>

### <span data-ttu-id="52efa-139">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscercertificate Atedescription</span><span class="sxs-lookup"><span data-stu-id="52efa-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="52efa-140">System. String</span><span class="sxs-lookup"><span data-stu-id="52efa-140">System.String</span></span>

## <span data-ttu-id="52efa-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52efa-141">OUTPUTS</span></span>

### <span data-ttu-id="52efa-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52efa-142">System.Boolean</span></span>

## <span data-ttu-id="52efa-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52efa-143">NOTES</span></span>

## <span data-ttu-id="52efa-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52efa-144">RELATED LINKS</span></span>
