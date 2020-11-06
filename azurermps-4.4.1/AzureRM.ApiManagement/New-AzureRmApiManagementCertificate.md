---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 55b95cec3e699872688fad5daeb0d2f7e89059c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591228"
---
# <span data-ttu-id="77c2f-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="77c2f-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="77c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="77c2f-103">Arka uç doğrulama sırasında kullanılacak bir API yönetim sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="77c2f-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77c2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="77c2f-104">SYNTAX</span></span>

### <span data-ttu-id="77c2f-105">Dosyadan yükleme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="77c2f-105">Load from file (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77c2f-106">Ham</span><span class="sxs-lookup"><span data-stu-id="77c2f-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77c2f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="77c2f-107">DESCRIPTION</span></span>
<span data-ttu-id="77c2f-108">**Yeni-Azurermapsananagementcertificate** cmdlet 'ı BIR Azure API yönetim sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="77c2f-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="77c2f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="77c2f-109">EXAMPLES</span></span>

### <span data-ttu-id="77c2f-110">Örnek 1: sertifika oluşturma ve yükleme</span><span class="sxs-lookup"><span data-stu-id="77c2f-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="77c2f-111">Bu komut bir API yönetim sertifikası oluşturur ve yükler.</span><span class="sxs-lookup"><span data-stu-id="77c2f-111">This command creates an API Management certificate and uploads it.</span></span>

## <span data-ttu-id="77c2f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="77c2f-112">PARAMETERS</span></span>

### <span data-ttu-id="77c2f-113">-Certificateıd</span><span class="sxs-lookup"><span data-stu-id="77c2f-113">-CertificateId</span></span>
<span data-ttu-id="77c2f-114">Oluşturulacak sertifikanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="77c2f-114">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="77c2f-115">Bu parametreyi belirtmezseniz, sizin için bir KIMLIK oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="77c2f-115">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="77c2f-116">-Context</span><span class="sxs-lookup"><span data-stu-id="77c2f-116">-Context</span></span>
<span data-ttu-id="77c2f-117">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="77c2f-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="77c2f-118">-Pfxbaytı</span><span class="sxs-lookup"><span data-stu-id="77c2f-118">-PfxBytes</span></span>
<span data-ttu-id="77c2f-119">Sertifika dosyasının,. pfx biçimindeki bir bayt dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="77c2f-119">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="77c2f-120">*Pfxdosyayolu* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="77c2f-120">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="77c2f-121">-Pfxdosyayolu</span><span class="sxs-lookup"><span data-stu-id="77c2f-121">-PfxFilePath</span></span>
<span data-ttu-id="77c2f-122">Oluşturulacak ve yüklenecek sertifika dosyasının yolunu. pfx biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="77c2f-122">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="77c2f-123">*Pfxbytes* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="77c2f-123">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Load from file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77c2f-124">-Pfxparolası</span><span class="sxs-lookup"><span data-stu-id="77c2f-124">-PfxPassword</span></span>
<span data-ttu-id="77c2f-125">Sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="77c2f-125">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="77c2f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c2f-126">-DefaultProfile</span></span>
<span data-ttu-id="77c2f-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="77c2f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77c2f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c2f-128">CommonParameters</span></span>
<span data-ttu-id="77c2f-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="77c2f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c2f-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77c2f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c2f-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="77c2f-131">INPUTS</span></span>

## <span data-ttu-id="77c2f-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="77c2f-132">OUTPUTS</span></span>

### <span data-ttu-id="77c2f-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="77c2f-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="77c2f-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="77c2f-134">NOTES</span></span>

## <span data-ttu-id="77c2f-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="77c2f-135">RELATED LINKS</span></span>

[<span data-ttu-id="77c2f-136">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="77c2f-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="77c2f-137">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="77c2f-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="77c2f-138">Set-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="77c2f-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


