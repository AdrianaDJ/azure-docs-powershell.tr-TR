---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: ca9305b2d5863276c5d898e310dfab8be7488382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764278"
---
# <span data-ttu-id="79a7a-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="79a7a-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="79a7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="79a7a-103">Bir API yönetim sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="79a7a-103">Modifies an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79a7a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79a7a-104">SYNTAX</span></span>

### <span data-ttu-id="79a7a-105">Dosyadan yükleme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79a7a-105">Load from file (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79a7a-106">Ham</span><span class="sxs-lookup"><span data-stu-id="79a7a-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79a7a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="79a7a-107">DESCRIPTION</span></span>
<span data-ttu-id="79a7a-108">**Set-Azurermapımanagementcertificate** cmdlet 'ı BIR Azure API yönetim sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="79a7a-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="79a7a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79a7a-109">EXAMPLES</span></span>

### <span data-ttu-id="79a7a-110">Örnek 1: sertifikayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="79a7a-110">Example 1: Modify a certificate</span></span>
```
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="79a7a-111">Bu komut belirtilen API yönetim sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="79a7a-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="79a7a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79a7a-112">PARAMETERS</span></span>

### <span data-ttu-id="79a7a-113">-Certificateıd</span><span class="sxs-lookup"><span data-stu-id="79a7a-113">-CertificateId</span></span>
<span data-ttu-id="79a7a-114">Değiştirilecek sertifikanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="79a7a-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="79a7a-115">-Context</span><span class="sxs-lookup"><span data-stu-id="79a7a-115">-Context</span></span>
<span data-ttu-id="79a7a-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79a7a-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="79a7a-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="79a7a-117">-PassThru</span></span>
<span data-ttu-id="79a7a-118">geçiş</span><span class="sxs-lookup"><span data-stu-id="79a7a-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a7a-119">-Pfxbaytı</span><span class="sxs-lookup"><span data-stu-id="79a7a-119">-PfxBytes</span></span>
<span data-ttu-id="79a7a-120">Sertifika dosyasının,. pfx biçimindeki bir bayt dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79a7a-120">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="79a7a-121">*Pfxdosyayolu* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="79a7a-121">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="79a7a-122">-Pfxdosyayolu</span><span class="sxs-lookup"><span data-stu-id="79a7a-122">-PfxFilePath</span></span>
<span data-ttu-id="79a7a-123">Oluşturulacak ve yüklenecek sertifika dosyasının yolunu. pfx biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="79a7a-123">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="79a7a-124">*Pfxbytes* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="79a7a-124">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="79a7a-125">-Pfxparolası</span><span class="sxs-lookup"><span data-stu-id="79a7a-125">-PfxPassword</span></span>
<span data-ttu-id="79a7a-126">Sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79a7a-126">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="79a7a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a7a-127">-DefaultProfile</span></span>
<span data-ttu-id="79a7a-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79a7a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79a7a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a7a-129">CommonParameters</span></span>
<span data-ttu-id="79a7a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79a7a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a7a-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79a7a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a7a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79a7a-132">INPUTS</span></span>

## <span data-ttu-id="79a7a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79a7a-133">OUTPUTS</span></span>

### <span data-ttu-id="79a7a-134">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="79a7a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="79a7a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79a7a-135">NOTES</span></span>

## <span data-ttu-id="79a7a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79a7a-136">RELATED LINKS</span></span>

[<span data-ttu-id="79a7a-137">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="79a7a-137">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="79a7a-138">Yeni-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="79a7a-138">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="79a7a-139">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="79a7a-139">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


