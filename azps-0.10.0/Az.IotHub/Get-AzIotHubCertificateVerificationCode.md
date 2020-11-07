---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: d4a9d20981c9777e02fd22e1dbbb70b24e91e282
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935845"
---
# <span data-ttu-id="2c9c2-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="2c9c2-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="2c9c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c9c2-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9c2-103">Azure IoT Hub sertifikası için doğrulama kodu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="2c9c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c9c2-104">SYNTAX</span></span>

### <span data-ttu-id="2c9c2-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2c9c2-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c9c2-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="2c9c2-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c9c2-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="2c9c2-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c9c2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c9c2-108">DESCRIPTION</span></span>
<span data-ttu-id="2c9c2-109">Bu doğrulama kodu, sertifika için bir özgünlük adımını tamamlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="2c9c2-110">Kök sertifikaları özel anahtarıyla imzaladığınız yeni bir sertifikanın CN 'si olarak bu doğrulama kodunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="2c9c2-111">Azure IoT Hub 'daki CA sertifikalarının ayrıntılı açıklaması için bkz: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="2c9c2-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="2c9c2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c9c2-112">EXAMPLES</span></span>

### <span data-ttu-id="2c9c2-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2c9c2-113">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
VerificationCode    : 47292AB6260DB02CCD2D07C601B7303DD49858B6
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="2c9c2-114">MyCertificate için doğrulama kodu oluşturur</span><span class="sxs-lookup"><span data-stu-id="2c9c2-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="2c9c2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c9c2-115">PARAMETERS</span></span>

### <span data-ttu-id="2c9c2-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2c9c2-116">-CertificateName</span></span>
<span data-ttu-id="2c9c2-117">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="2c9c2-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="2c9c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9c2-118">-DefaultProfile</span></span>
<span data-ttu-id="2c9c2-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c9c2-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="2c9c2-120">-Etag</span></span>
<span data-ttu-id="2c9c2-121">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="2c9c2-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="2c9c2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c9c2-122">-InputObject</span></span>
<span data-ttu-id="2c9c2-123">Sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="2c9c2-123">Certificate Object</span></span>

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

### <span data-ttu-id="2c9c2-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c9c2-124">-Name</span></span>
<span data-ttu-id="2c9c2-125">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="2c9c2-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2c9c2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c9c2-126">-ResourceGroupName</span></span>
<span data-ttu-id="2c9c2-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2c9c2-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2c9c2-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2c9c2-128">-ResourceId</span></span>
<span data-ttu-id="2c9c2-129">Sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2c9c2-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="2c9c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9c2-130">CommonParameters</span></span>
<span data-ttu-id="2c9c2-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9c2-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9c2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9c2-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c9c2-133">INPUTS</span></span>

### <span data-ttu-id="2c9c2-134">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscercertificate Atedescription</span><span class="sxs-lookup"><span data-stu-id="2c9c2-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="2c9c2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2c9c2-135">System.String</span></span>

## <span data-ttu-id="2c9c2-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c9c2-136">OUTPUTS</span></span>

### <span data-ttu-id="2c9c2-137">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscercertificate Atewithnoncedescription</span><span class="sxs-lookup"><span data-stu-id="2c9c2-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="2c9c2-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c9c2-138">NOTES</span></span>

## <span data-ttu-id="2c9c2-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c9c2-139">RELATED LINKS</span></span>
