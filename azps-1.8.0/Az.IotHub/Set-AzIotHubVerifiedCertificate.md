---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 868ca6f3f9f65fea5fd04dba1fc19d4db11bd65c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916399"
---
# <span data-ttu-id="044a5-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="044a5-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="044a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="044a5-102">SYNOPSIS</span></span>
<span data-ttu-id="044a5-103">Bir Azure IoT Hub sertifikasını doğrular.</span><span class="sxs-lookup"><span data-stu-id="044a5-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="044a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="044a5-104">SYNTAX</span></span>

### <span data-ttu-id="044a5-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="044a5-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="044a5-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="044a5-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="044a5-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="044a5-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="044a5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="044a5-108">DESCRIPTION</span></span>
<span data-ttu-id="044a5-109">Get-Aziothubcertificatedoðrulamasý Icationcode cmdlet 'i tarafından alınan doğrulama kodunu içeren bir doğrulama sertifikası yükleyerek sertifikayı doğrular.</span><span class="sxs-lookup"><span data-stu-id="044a5-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="044a5-110">Bu, elinde bulunan en son adımdır.</span><span class="sxs-lookup"><span data-stu-id="044a5-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="044a5-111">Azure IoT Hub 'daki CA sertifikalarının ayrıntılı açıklaması için bkz: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="044a5-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="044a5-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="044a5-112">EXAMPLES</span></span>

### <span data-ttu-id="044a5-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="044a5-113">Example 1</span></span>
```
PS C:\> Set-AzIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="044a5-114">MyCertificate özel anahtarının sahipliğini doğrular.</span><span class="sxs-lookup"><span data-stu-id="044a5-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="044a5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="044a5-115">PARAMETERS</span></span>

### <span data-ttu-id="044a5-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="044a5-116">-CertificateName</span></span>
<span data-ttu-id="044a5-117">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="044a5-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="044a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="044a5-118">-DefaultProfile</span></span>
<span data-ttu-id="044a5-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="044a5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="044a5-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="044a5-120">-Etag</span></span>
<span data-ttu-id="044a5-121">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="044a5-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="044a5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="044a5-122">-InputObject</span></span>
<span data-ttu-id="044a5-123">Sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="044a5-123">Certificate Object</span></span>

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

### <span data-ttu-id="044a5-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="044a5-124">-Name</span></span>
<span data-ttu-id="044a5-125">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="044a5-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="044a5-126">-Yol</span><span class="sxs-lookup"><span data-stu-id="044a5-126">-Path</span></span>
<span data-ttu-id="044a5-127">x509 Certificate. cer dosyasının veya. pem dosya yolunun Base-64 temsili.</span><span class="sxs-lookup"><span data-stu-id="044a5-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="044a5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="044a5-128">-ResourceGroupName</span></span>
<span data-ttu-id="044a5-129">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="044a5-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="044a5-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="044a5-130">-ResourceId</span></span>
<span data-ttu-id="044a5-131">Sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="044a5-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="044a5-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="044a5-132">-Confirm</span></span>
<span data-ttu-id="044a5-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="044a5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="044a5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="044a5-134">-WhatIf</span></span>
<span data-ttu-id="044a5-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="044a5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="044a5-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="044a5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="044a5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044a5-137">CommonParameters</span></span>
<span data-ttu-id="044a5-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="044a5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044a5-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="044a5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044a5-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="044a5-140">INPUTS</span></span>

### <span data-ttu-id="044a5-141">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscercertificate Atedescription</span><span class="sxs-lookup"><span data-stu-id="044a5-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="044a5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="044a5-142">System.String</span></span>

## <span data-ttu-id="044a5-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="044a5-143">OUTPUTS</span></span>

### <span data-ttu-id="044a5-144">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscercertificate Atedescription</span><span class="sxs-lookup"><span data-stu-id="044a5-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="044a5-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="044a5-145">NOTES</span></span>

## <span data-ttu-id="044a5-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="044a5-146">RELATED LINKS</span></span>
