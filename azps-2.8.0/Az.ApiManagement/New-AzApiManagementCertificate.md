---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
ms.openlocfilehash: e2f32bc5d05121411a109c1371b52b41843cfc56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753532"
---
# <span data-ttu-id="bbe96-101">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="bbe96-101">New-AzApiManagementCertificate</span></span>

## <span data-ttu-id="bbe96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbe96-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe96-103">Arka uç doğrulama sırasında kullanılacak bir API yönetim sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bbe96-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

## <span data-ttu-id="bbe96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbe96-104">SYNTAX</span></span>

### <span data-ttu-id="bbe96-105">LoadFromFile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bbe96-105">LoadFromFile (Default)</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbe96-106">Ham</span><span class="sxs-lookup"><span data-stu-id="bbe96-106">Raw</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>] -PfxBytes <Byte[]>
 -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbe96-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbe96-107">DESCRIPTION</span></span>
<span data-ttu-id="bbe96-108">**Yeni-Azapsananagementcertificate** cmdlet 'ı BIR Azure API yönetim sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bbe96-108">The **New-AzApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="bbe96-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbe96-109">EXAMPLES</span></span>

### <span data-ttu-id="bbe96-110">Örnek 1: sertifika oluşturma ve yükleme</span><span class="sxs-lookup"><span data-stu-id="bbe96-110">Example 1: Create and upload a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="bbe96-111">Bu komut, bir sertifikayı API yönetimine yükler.</span><span class="sxs-lookup"><span data-stu-id="bbe96-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="bbe96-112">Bu sertifika, ilkeleri kullanarak arka uç ile karşılıklı kimlik doğrulama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bbe96-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="bbe96-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbe96-113">PARAMETERS</span></span>

### <span data-ttu-id="bbe96-114">-Certificateıd</span><span class="sxs-lookup"><span data-stu-id="bbe96-114">-CertificateId</span></span>
<span data-ttu-id="bbe96-115">Oluşturulacak sertifikanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbe96-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="bbe96-116">Bu parametreyi belirtmezseniz, sizin için bir KIMLIK oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bbe96-116">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="bbe96-117">-Context</span><span class="sxs-lookup"><span data-stu-id="bbe96-117">-Context</span></span>
<span data-ttu-id="bbe96-118">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbe96-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe96-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe96-119">-DefaultProfile</span></span>
<span data-ttu-id="bbe96-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bbe96-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbe96-121">-Pfxbaytı</span><span class="sxs-lookup"><span data-stu-id="bbe96-121">-PfxBytes</span></span>
<span data-ttu-id="bbe96-122">Sertifika dosyasının,. pfx biçimindeki bir bayt dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbe96-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="bbe96-123">*Pfxdosyayolu* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="bbe96-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="bbe96-124">-Pfxdosyayolu</span><span class="sxs-lookup"><span data-stu-id="bbe96-124">-PfxFilePath</span></span>
<span data-ttu-id="bbe96-125">Oluşturulacak ve yüklenecek sertifika dosyasının yolunu. pfx biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbe96-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="bbe96-126">*Pfxbytes* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="bbe96-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="bbe96-127">-Pfxparolası</span><span class="sxs-lookup"><span data-stu-id="bbe96-127">-PfxPassword</span></span>
<span data-ttu-id="bbe96-128">Sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbe96-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="bbe96-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe96-129">CommonParameters</span></span>
<span data-ttu-id="bbe96-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbe96-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe96-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bbe96-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe96-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbe96-132">INPUTS</span></span>

### <span data-ttu-id="bbe96-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="bbe96-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bbe96-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bbe96-134">System.String</span></span>

### <span data-ttu-id="bbe96-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="bbe96-135">System.Byte[]</span></span>

## <span data-ttu-id="bbe96-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbe96-136">OUTPUTS</span></span>

### <span data-ttu-id="bbe96-137">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="bbe96-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="bbe96-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbe96-138">NOTES</span></span>

## <span data-ttu-id="bbe96-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbe96-139">RELATED LINKS</span></span>

[<span data-ttu-id="bbe96-140">Get-Azsız sertifika</span><span class="sxs-lookup"><span data-stu-id="bbe96-140">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="bbe96-141">Remove-Azapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="bbe96-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="bbe96-142">Set-Azapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="bbe96-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


