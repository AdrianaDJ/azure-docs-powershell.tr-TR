---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 6d77bcc6d940c5891b4fc06875dc353af5f75939
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277793"
---
# <span data-ttu-id="b0900-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="b0900-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="b0900-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0900-102">SYNOPSIS</span></span>
<span data-ttu-id="b0900-103">Bir Azure IoT Hub sertifikası oluşturun/güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="b0900-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="b0900-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0900-104">SYNTAX</span></span>

### <span data-ttu-id="b0900-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b0900-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0900-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="b0900-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0900-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="b0900-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0900-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0900-108">DESCRIPTION</span></span>
<span data-ttu-id="b0900-109">Yeni bir sertifikayı karşıya yükler veya varolan sertifikayı aynı adla değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b0900-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="b0900-110">Azure IoT Hub 'daki CA sertifikalarının ayrıntılı açıklaması için bkz: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="b0900-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="b0900-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0900-111">EXAMPLES</span></span>

### <span data-ttu-id="b0900-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b0900-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="b0900-113">Bir CA sertifika CER dosyasını IoT Hub 'ına yükler.</span><span class="sxs-lookup"><span data-stu-id="b0900-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="b0900-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b0900-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="b0900-115">Yeni bir CER dosyası yükleyerek bir IoT Hub 'ındaki CA sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b0900-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="b0900-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0900-116">PARAMETERS</span></span>

### <span data-ttu-id="b0900-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b0900-117">-CertificateName</span></span>
<span data-ttu-id="b0900-118">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="b0900-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="b0900-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0900-119">-DefaultProfile</span></span>
<span data-ttu-id="b0900-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b0900-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0900-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="b0900-121">-Etag</span></span>
<span data-ttu-id="b0900-122">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="b0900-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="b0900-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0900-123">-InputObject</span></span>
<span data-ttu-id="b0900-124">Sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="b0900-124">Certificate Object</span></span>

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

### <span data-ttu-id="b0900-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="b0900-125">-Name</span></span>
<span data-ttu-id="b0900-126">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="b0900-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b0900-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="b0900-127">-Path</span></span>
<span data-ttu-id="b0900-128">x509 Certificate. cer dosyasının veya. pem dosya yolunun Base-64 temsili.</span><span class="sxs-lookup"><span data-stu-id="b0900-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0900-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0900-129">-ResourceGroupName</span></span>
<span data-ttu-id="b0900-130">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b0900-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b0900-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b0900-131">-ResourceId</span></span>
<span data-ttu-id="b0900-132">Sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b0900-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="b0900-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="b0900-133">-Confirm</span></span>
<span data-ttu-id="b0900-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b0900-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0900-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0900-135">-WhatIf</span></span>
<span data-ttu-id="b0900-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b0900-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0900-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b0900-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0900-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0900-138">CommonParameters</span></span>
<span data-ttu-id="b0900-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0900-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0900-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0900-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0900-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0900-141">INPUTS</span></span>

### <span data-ttu-id="b0900-142">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscercertificate Atedescription</span><span class="sxs-lookup"><span data-stu-id="b0900-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="b0900-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b0900-143">System.String</span></span>

## <span data-ttu-id="b0900-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0900-144">OUTPUTS</span></span>

### <span data-ttu-id="b0900-145">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscercertificate Atedescription</span><span class="sxs-lookup"><span data-stu-id="b0900-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="b0900-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0900-146">NOTES</span></span>

## <span data-ttu-id="b0900-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0900-147">RELATED LINKS</span></span>
