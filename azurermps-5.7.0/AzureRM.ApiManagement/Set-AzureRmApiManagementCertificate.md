---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 1b1f16c8d48debb04ad1f38c03aa58e65f9953a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590542"
---
# <span data-ttu-id="913b6-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="913b6-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="913b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="913b6-102">SYNOPSIS</span></span>
<span data-ttu-id="913b6-103">Arka uç ile karşılıklı kimlik doğrulama için yapılandırılmış bir API yönetim sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="913b6-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="913b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="913b6-104">SYNTAX</span></span>

### <span data-ttu-id="913b6-105">LoadFromFile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="913b6-105">LoadFromFile (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="913b6-106">Ham</span><span class="sxs-lookup"><span data-stu-id="913b6-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="913b6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="913b6-107">DESCRIPTION</span></span>
<span data-ttu-id="913b6-108">**Set-Azurermapımanagementcertificate** cmdlet 'ı BIR Azure API yönetim sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="913b6-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="913b6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="913b6-109">EXAMPLES</span></span>

### <span data-ttu-id="913b6-110">Örnek 1: sertifikayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="913b6-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="913b6-111">Bu komut belirtilen API yönetim sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="913b6-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="913b6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="913b6-112">PARAMETERS</span></span>

### <span data-ttu-id="913b6-113">-Certificateıd</span><span class="sxs-lookup"><span data-stu-id="913b6-113">-CertificateId</span></span>
<span data-ttu-id="913b6-114">Değiştirilecek sertifikanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b6-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="913b6-115">-Context</span><span class="sxs-lookup"><span data-stu-id="913b6-115">-Context</span></span>
<span data-ttu-id="913b6-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b6-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="913b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913b6-117">-DefaultProfile</span></span>
<span data-ttu-id="913b6-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="913b6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="913b6-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="913b6-119">-PassThru</span></span>
<span data-ttu-id="913b6-120">geçiş</span><span class="sxs-lookup"><span data-stu-id="913b6-120">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913b6-121">-Pfxbaytı</span><span class="sxs-lookup"><span data-stu-id="913b6-121">-PfxBytes</span></span>
<span data-ttu-id="913b6-122">Sertifika dosyasının,. pfx biçimindeki bir bayt dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b6-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="913b6-123">*Pfxdosyayolu* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="913b6-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="913b6-124">-Pfxdosyayolu</span><span class="sxs-lookup"><span data-stu-id="913b6-124">-PfxFilePath</span></span>
<span data-ttu-id="913b6-125">Oluşturulacak ve yüklenecek sertifika dosyasının yolunu. pfx biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b6-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="913b6-126">*Pfxbytes* parametresini belirtmezseniz bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="913b6-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="913b6-127">-Pfxparolası</span><span class="sxs-lookup"><span data-stu-id="913b6-127">-PfxPassword</span></span>
<span data-ttu-id="913b6-128">Sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b6-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="913b6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913b6-129">CommonParameters</span></span>
<span data-ttu-id="913b6-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="913b6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913b6-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="913b6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913b6-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="913b6-132">INPUTS</span></span>

### <span data-ttu-id="913b6-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="913b6-133">None</span></span>
<span data-ttu-id="913b6-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="913b6-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="913b6-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="913b6-135">OUTPUTS</span></span>

### <span data-ttu-id="913b6-136">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcertificate</span><span class="sxs-lookup"><span data-stu-id="913b6-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="913b6-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="913b6-137">NOTES</span></span>

## <span data-ttu-id="913b6-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="913b6-138">RELATED LINKS</span></span>

[<span data-ttu-id="913b6-139">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="913b6-139">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="913b6-140">Yeni-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="913b6-140">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="913b6-141">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="913b6-141">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


