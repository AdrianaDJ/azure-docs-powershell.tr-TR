---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f97f6c59bc1888f511d84ed49e6d1d49a5d7f57f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588640"
---
# <span data-ttu-id="2653e-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2653e-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="2653e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2653e-102">SYNOPSIS</span></span>
<span data-ttu-id="2653e-103">Arka uç doğrulama sırasında kullanılacak bir API yönetim sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2653e-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2653e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2653e-104">SYNTAX</span></span>

### <span data-ttu-id="2653e-105">LoadFromFile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2653e-105">LoadFromFile (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2653e-106">Ham</span><span class="sxs-lookup"><span data-stu-id="2653e-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2653e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2653e-107">DESCRIPTION</span></span>
<span data-ttu-id="2653e-108">**Yeni-Azurermapsananagementcertificate** cmdlet 'ı BIR Azure API yönetim sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2653e-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="2653e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2653e-109">EXAMPLES</span></span>

### <span data-ttu-id="2653e-110">Örnek 1: sertifika oluşturma ve yükleme</span><span class="sxs-lookup"><span data-stu-id="2653e-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="2653e-111">Bu komut, bir sertifikayı API yönetimine yükler.</span><span class="sxs-lookup"><span data-stu-id="2653e-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="2653e-112">Bu sertifika, ilkeleri kullanarak arka uç ile karşılıklı kimlik doğrulama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2653e-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="2653e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2653e-113">PARAMETERS</span></span>

### <span data-ttu-id="2653e-114">-Certificateıd</span><span class="sxs-lookup"><span data-stu-id="2653e-114">-CertificateId</span></span>
<span data-ttu-id="2653e-115">Oluşturulacak sertifikanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2653e-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="2653e-116">Bu parametreyi belirtmezseniz, sizin için bir KIMLIK oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2653e-116">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2653e-117">-Context</span><span class="sxs-lookup"><span data-stu-id="2653e-117">-Context</span></span>
<span data-ttu-id="2653e-118">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2653e-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2653e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2653e-119">-DefaultProfile</span></span>
<span data-ttu-id="2653e-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2653e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2653e-121">-Pfxbaytı</span><span class="sxs-lookup"><span data-stu-id="2653e-121">-PfxBytes</span></span>
<span data-ttu-id="2653e-122">Sertifika dosyasının,. pfx biçimindeki bir bayt dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2653e-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="2653e-123">*Pfxdosyayolu* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2653e-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2653e-124">-Pfxdosyayolu</span><span class="sxs-lookup"><span data-stu-id="2653e-124">-PfxFilePath</span></span>
<span data-ttu-id="2653e-125">Oluşturulacak ve yüklenecek sertifika dosyasının yolunu. pfx biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="2653e-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="2653e-126">*Pfxbytes* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2653e-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2653e-127">-Pfxparolası</span><span class="sxs-lookup"><span data-stu-id="2653e-127">-PfxPassword</span></span>
<span data-ttu-id="2653e-128">Sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2653e-128">Specifies the password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2653e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2653e-129">CommonParameters</span></span>
<span data-ttu-id="2653e-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2653e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2653e-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2653e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2653e-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2653e-132">INPUTS</span></span>

### <span data-ttu-id="2653e-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="2653e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2653e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2653e-134">System.String</span></span>

### <span data-ttu-id="2653e-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="2653e-135">System.Byte[]</span></span>

## <span data-ttu-id="2653e-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2653e-136">OUTPUTS</span></span>

### <span data-ttu-id="2653e-137">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="2653e-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="2653e-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2653e-138">NOTES</span></span>

## <span data-ttu-id="2653e-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2653e-139">RELATED LINKS</span></span>

[<span data-ttu-id="2653e-140">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="2653e-140">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="2653e-141">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="2653e-141">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="2653e-142">Set-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="2653e-142">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


