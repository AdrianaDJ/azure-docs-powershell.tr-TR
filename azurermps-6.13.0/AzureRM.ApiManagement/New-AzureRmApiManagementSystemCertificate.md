---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
ms.openlocfilehash: fa64e9bade3a6cd8ec4edc8e04956c97306328ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573078"
---
# <span data-ttu-id="1d6b6-101">New-AzureRmApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="1d6b6-101">New-AzureRmApiManagementSystemCertificate</span></span>

## <span data-ttu-id="1d6b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d6b6-102">SYNOPSIS</span></span>
<span data-ttu-id="1d6b6-103">Örneği oluşturur `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="1d6b6-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="1d6b6-104">Sertifika özel CA 'lar tarafından verilebilir ve API Yönetim hizmetine `CertificateAuthority` veya depolama uygulamasına yüklenir `Root` .</span><span class="sxs-lookup"><span data-stu-id="1d6b6-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d6b6-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d6b6-105">SYNTAX</span></span>

```
New-AzureRmApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d6b6-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d6b6-106">DESCRIPTION</span></span>
<span data-ttu-id="1d6b6-107">**New-AzureRmApiManagementSystemCertificate** cmdlet 'i, bir **PsApiManagementSystemCertificate** örneği oluşturan yardımcı komuttur.</span><span class="sxs-lookup"><span data-stu-id="1d6b6-107">The **New-AzureRmApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="1d6b6-108">Bu komut New-AzureRmApiManagement ve Set-AzureRmApiManagement cmdlet 'inde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1d6b6-108">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="1d6b6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d6b6-109">EXAMPLES</span></span>

### <span data-ttu-id="1d6b6-110">Örnek 1: dosyadan SSL sertifikası kullanarak PsApiManagementSystemCertificate örneğini oluşturma ve başlatma</span><span class="sxs-lookup"><span data-stu-id="1d6b6-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzureRmApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="1d6b6-111">Bu komut, kök CA sertifikasıyla bir **PsApiManagementSystemCertificate** örneğini oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="1d6b6-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="1d6b6-112">Ardından, CA yetkilisini kök mağazaya yükleyen API yönetim hizmeti oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1d6b6-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="1d6b6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d6b6-113">PARAMETERS</span></span>

### <span data-ttu-id="1d6b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d6b6-114">-DefaultProfile</span></span>
<span data-ttu-id="1d6b6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d6b6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d6b6-116">-Pfxparolası</span><span class="sxs-lookup"><span data-stu-id="1d6b6-116">-PfxPassword</span></span>
<span data-ttu-id="1d6b6-117">. Pfx sertifika dosyasının parolası.</span><span class="sxs-lookup"><span data-stu-id="1d6b6-117">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d6b6-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="1d6b6-118">-PfxPath</span></span>
<span data-ttu-id="1d6b6-119">. Pfx sertifika dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="1d6b6-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="1d6b6-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="1d6b6-120">-StoreName</span></span>
<span data-ttu-id="1d6b6-121">Sertifika StoreName</span><span class="sxs-lookup"><span data-stu-id="1d6b6-121">Certificate StoreName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d6b6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d6b6-122">CommonParameters</span></span>
<span data-ttu-id="1d6b6-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d6b6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d6b6-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d6b6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d6b6-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d6b6-125">INPUTS</span></span>

### <span data-ttu-id="1d6b6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1d6b6-126">System.String</span></span>

### <span data-ttu-id="1d6b6-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1d6b6-127">System.Security.SecureString</span></span>

## <span data-ttu-id="1d6b6-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d6b6-128">OUTPUTS</span></span>

### <span data-ttu-id="1d6b6-129">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="1d6b6-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="1d6b6-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d6b6-130">NOTES</span></span>

## <span data-ttu-id="1d6b6-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d6b6-131">RELATED LINKS</span></span>

[<span data-ttu-id="1d6b6-132">Yeni-azurermapı</span><span class="sxs-lookup"><span data-stu-id="1d6b6-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="1d6b6-133">Set-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="1d6b6-133">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
