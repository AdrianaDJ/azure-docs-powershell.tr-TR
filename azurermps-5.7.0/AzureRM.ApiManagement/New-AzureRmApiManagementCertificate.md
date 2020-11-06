---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f7ddfb327931fc7ebb9eac76cdd6818521332483
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589911"
---
# <span data-ttu-id="db130-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="db130-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="db130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db130-102">SYNOPSIS</span></span>
<span data-ttu-id="db130-103">Arka uç doğrulama sırasında kullanılacak bir API yönetim sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="db130-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db130-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db130-104">SYNTAX</span></span>

### <span data-ttu-id="db130-105">LoadFromFile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="db130-105">LoadFromFile (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db130-106">Ham</span><span class="sxs-lookup"><span data-stu-id="db130-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db130-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="db130-107">DESCRIPTION</span></span>
<span data-ttu-id="db130-108">**Yeni-Azurermapsananagementcertificate** cmdlet 'ı BIR Azure API yönetim sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="db130-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="db130-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db130-109">EXAMPLES</span></span>

### <span data-ttu-id="db130-110">Örnek 1: sertifika oluşturma ve yükleme</span><span class="sxs-lookup"><span data-stu-id="db130-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="db130-111">Bu komut, bir sertifikayı API yönetimine yükler.</span><span class="sxs-lookup"><span data-stu-id="db130-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="db130-112">Bu sertifika, ilkeleri kullanarak arka uç ile karşılıklı kimlik doğrulama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="db130-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="db130-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db130-113">PARAMETERS</span></span>

### <span data-ttu-id="db130-114">-Certificateıd</span><span class="sxs-lookup"><span data-stu-id="db130-114">-CertificateId</span></span>
<span data-ttu-id="db130-115">Oluşturulacak sertifikanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="db130-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="db130-116">Bu parametreyi belirtmezseniz, sizin için bir KIMLIK oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="db130-116">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db130-117">-Context</span><span class="sxs-lookup"><span data-stu-id="db130-117">-Context</span></span>
<span data-ttu-id="db130-118">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db130-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db130-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db130-119">-DefaultProfile</span></span>
<span data-ttu-id="db130-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db130-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="db130-121">-Pfxbaytı</span><span class="sxs-lookup"><span data-stu-id="db130-121">-PfxBytes</span></span>
<span data-ttu-id="db130-122">Sertifika dosyasının,. pfx biçimindeki bir bayt dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db130-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="db130-123">*Pfxdosyayolu* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="db130-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db130-124">-Pfxdosyayolu</span><span class="sxs-lookup"><span data-stu-id="db130-124">-PfxFilePath</span></span>
<span data-ttu-id="db130-125">Oluşturulacak ve yüklenecek sertifika dosyasının yolunu. pfx biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="db130-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="db130-126">*Pfxbytes* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="db130-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: LoadFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db130-127">-Pfxparolası</span><span class="sxs-lookup"><span data-stu-id="db130-127">-PfxPassword</span></span>
<span data-ttu-id="db130-128">Sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db130-128">Specifies the password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db130-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db130-129">CommonParameters</span></span>
<span data-ttu-id="db130-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db130-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db130-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db130-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db130-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db130-132">INPUTS</span></span>

### <span data-ttu-id="db130-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="db130-133">None</span></span>
<span data-ttu-id="db130-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="db130-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db130-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db130-135">OUTPUTS</span></span>

### <span data-ttu-id="db130-136">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="db130-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="db130-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db130-137">NOTES</span></span>

## <span data-ttu-id="db130-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db130-138">RELATED LINKS</span></span>

[<span data-ttu-id="db130-139">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="db130-139">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="db130-140">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="db130-140">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="db130-141">Set-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="db130-141">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


