---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
ms.openlocfilehash: 55cd14216e9a592128c8d600238b49862cb1f20a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590468"
---
# <span data-ttu-id="2da04-101">Get-AzureRmIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="2da04-101">Get-AzureRmIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="2da04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2da04-102">SYNOPSIS</span></span>
<span data-ttu-id="2da04-103">Azure IoT Hub sertifikası için doğrulama kodu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2da04-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2da04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2da04-104">SYNTAX</span></span>

### <span data-ttu-id="2da04-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2da04-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da04-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="2da04-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da04-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="2da04-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2da04-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2da04-108">DESCRIPTION</span></span>
<span data-ttu-id="2da04-109">Bu doğrulama kodu, sertifika için bir özgünlük adımını tamamlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2da04-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="2da04-110">Kök sertifikaları özel anahtarıyla imzaladığınız yeni bir sertifikanın CN 'si olarak bu doğrulama kodunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="2da04-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="2da04-111">Azure IoT Hub 'daki CA sertifikalarının ayrıntılı açıklaması için bkz: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="2da04-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="2da04-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2da04-112">EXAMPLES</span></span>

### <span data-ttu-id="2da04-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2da04-113">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="2da04-114">MyCertificate için doğrulama kodu oluşturur</span><span class="sxs-lookup"><span data-stu-id="2da04-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="2da04-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2da04-115">PARAMETERS</span></span>

### <span data-ttu-id="2da04-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2da04-116">-CertificateName</span></span>
<span data-ttu-id="2da04-117">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="2da04-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="2da04-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da04-118">-DefaultProfile</span></span>
<span data-ttu-id="2da04-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2da04-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2da04-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="2da04-120">-Etag</span></span>
<span data-ttu-id="2da04-121">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="2da04-121">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da04-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2da04-122">-InputObject</span></span>
<span data-ttu-id="2da04-123">Sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="2da04-123">Certificate Object</span></span>

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

### <span data-ttu-id="2da04-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="2da04-124">-Name</span></span>
<span data-ttu-id="2da04-125">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="2da04-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2da04-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2da04-126">-ResourceGroupName</span></span>
<span data-ttu-id="2da04-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2da04-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2da04-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2da04-128">-ResourceId</span></span>
<span data-ttu-id="2da04-129">Sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2da04-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="2da04-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da04-130">CommonParameters</span></span>
<span data-ttu-id="2da04-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2da04-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da04-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2da04-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da04-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2da04-133">INPUTS</span></span>

### <span data-ttu-id="2da04-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2da04-134">System.String</span></span>

## <span data-ttu-id="2da04-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2da04-135">OUTPUTS</span></span>

### <span data-ttu-id="2da04-136">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscercertificate Atewithnoncedescription</span><span class="sxs-lookup"><span data-stu-id="2da04-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="2da04-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2da04-137">NOTES</span></span>

## <span data-ttu-id="2da04-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2da04-138">RELATED LINKS</span></span>

