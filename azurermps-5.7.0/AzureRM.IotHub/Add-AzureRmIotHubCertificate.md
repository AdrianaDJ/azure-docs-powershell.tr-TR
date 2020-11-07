---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubCertificate.md
ms.openlocfilehash: b38fd64db24a38267b3d06d8046f1bcbb826537f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763053"
---
# <span data-ttu-id="6f6f7-101">Add-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="6f6f7-101">Add-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="6f6f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f6f7-102">SYNOPSIS</span></span>
<span data-ttu-id="6f6f7-103">Bir Azure IoT Hub sertifikası oluşturun/güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="6f6f7-103">Create/update an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f6f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f6f7-104">SYNTAX</span></span>

### <span data-ttu-id="6f6f7-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f6f7-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f6f7-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="6f6f7-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f6f7-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="6f6f7-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f6f7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f6f7-108">DESCRIPTION</span></span>
<span data-ttu-id="6f6f7-109">Yeni bir sertifikayı karşıya yükler veya varolan sertifikayı aynı adla değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6f6f7-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="6f6f7-110">Azure IoT Hub 'daki CA sertifikalarının ayrıntılı açıklaması için bkz: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="6f6f7-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="6f6f7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f6f7-111">EXAMPLES</span></span>

### <span data-ttu-id="6f6f7-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6f6f7-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

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

<span data-ttu-id="6f6f7-113">Bir CA sertifika CER dosyasını IoT Hub 'ına yükler.</span><span class="sxs-lookup"><span data-stu-id="6f6f7-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="6f6f7-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6f6f7-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="6f6f7-115">Yeni bir CER dosyası yükleyerek bir IoT Hub 'ındaki CA sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6f6f7-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="6f6f7-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f6f7-116">PARAMETERS</span></span>

### <span data-ttu-id="6f6f7-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="6f6f7-117">-CertificateName</span></span>
<span data-ttu-id="6f6f7-118">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="6f6f7-118">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f6f7-119">-DefaultProfile</span></span>
<span data-ttu-id="6f6f7-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f6f7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f7-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="6f6f7-121">-Etag</span></span>
<span data-ttu-id="6f6f7-122">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="6f6f7-122">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f6f7-123">-InputObject</span></span>
<span data-ttu-id="6f6f7-124">Sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="6f6f7-124">Certificate Object</span></span>

```yaml
Type: PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f7-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="6f6f7-125">-Name</span></span>
<span data-ttu-id="6f6f7-126">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="6f6f7-126">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f7-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="6f6f7-127">-Path</span></span>
<span data-ttu-id="6f6f7-128">x509 Certificate. cer dosyasının veya. pem dosya yolunun Base-64 temsili.</span><span class="sxs-lookup"><span data-stu-id="6f6f7-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f6f7-129">-ResourceGroupName</span></span>
<span data-ttu-id="6f6f7-130">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="6f6f7-130">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f7-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6f6f7-131">-ResourceId</span></span>
<span data-ttu-id="6f6f7-132">Sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6f6f7-132">Certificate Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f7-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="6f6f7-133">-Confirm</span></span>
<span data-ttu-id="6f6f7-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6f6f7-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f6f7-135">-WhatIf</span></span>
<span data-ttu-id="6f6f7-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f6f7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f6f7-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6f6f7-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f6f7-138">CommonParameters</span></span>
<span data-ttu-id="6f6f7-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f6f7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f6f7-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f6f7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f6f7-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f6f7-141">INPUTS</span></span>

### <span data-ttu-id="6f6f7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6f6f7-142">System.String</span></span>

## <span data-ttu-id="6f6f7-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f6f7-143">OUTPUTS</span></span>

### <span data-ttu-id="6f6f7-144">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscercertificate Atedescription</span><span class="sxs-lookup"><span data-stu-id="6f6f7-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="6f6f7-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f6f7-145">NOTES</span></span>

## <span data-ttu-id="6f6f7-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f6f7-146">RELATED LINKS</span></span>

