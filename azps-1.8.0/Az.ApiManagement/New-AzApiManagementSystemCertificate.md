---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 54d2dba9c8db271fd495164049f2990a96a4b505
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917831"
---
# <span data-ttu-id="47af8-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="47af8-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="47af8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47af8-102">SYNOPSIS</span></span>
<span data-ttu-id="47af8-103">Örneği oluşturur `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="47af8-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="47af8-104">Sertifika özel CA 'lar tarafından verilebilir ve API Yönetim hizmetine `CertificateAuthority` veya depolama uygulamasına yüklenir `Root` .</span><span class="sxs-lookup"><span data-stu-id="47af8-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="47af8-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47af8-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47af8-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="47af8-106">DESCRIPTION</span></span>
<span data-ttu-id="47af8-107">**New-AzApiManagementSystemCertificate** cmdlet 'i, bir **PsApiManagementSystemCertificate** örneği oluşturan yardımcı komuttur.</span><span class="sxs-lookup"><span data-stu-id="47af8-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="47af8-108">Bu komut New-AzApiManagement ve Set-AzApiManagement cmdlet 'inde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="47af8-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="47af8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47af8-109">EXAMPLES</span></span>

### <span data-ttu-id="47af8-110">Örnek 1: dosyadan SSL sertifikası kullanarak PsApiManagementSystemCertificate örneğini oluşturma ve başlatma</span><span class="sxs-lookup"><span data-stu-id="47af8-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="47af8-111">Bu komut, kök CA sertifikasıyla bir **PsApiManagementSystemCertificate** örneğini oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="47af8-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="47af8-112">Ardından, CA yetkilisini kök mağazaya yükleyen API yönetim hizmeti oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="47af8-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="47af8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47af8-113">PARAMETERS</span></span>

### <span data-ttu-id="47af8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47af8-114">-DefaultProfile</span></span>
<span data-ttu-id="47af8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47af8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47af8-116">-Pfxparolası</span><span class="sxs-lookup"><span data-stu-id="47af8-116">-PfxPassword</span></span>
<span data-ttu-id="47af8-117">. Pfx sertifika dosyasının parolası.</span><span class="sxs-lookup"><span data-stu-id="47af8-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="47af8-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="47af8-118">-PfxPath</span></span>
<span data-ttu-id="47af8-119">. Pfx sertifika dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="47af8-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="47af8-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="47af8-120">-StoreName</span></span>
<span data-ttu-id="47af8-121">Sertifika StoreName</span><span class="sxs-lookup"><span data-stu-id="47af8-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="47af8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47af8-122">CommonParameters</span></span>
<span data-ttu-id="47af8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47af8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47af8-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47af8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47af8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47af8-125">INPUTS</span></span>

### <span data-ttu-id="47af8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="47af8-126">System.String</span></span>

### <span data-ttu-id="47af8-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="47af8-127">System.Security.SecureString</span></span>

## <span data-ttu-id="47af8-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47af8-128">OUTPUTS</span></span>

### <span data-ttu-id="47af8-129">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="47af8-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="47af8-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47af8-130">NOTES</span></span>

## <span data-ttu-id="47af8-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47af8-131">RELATED LINKS</span></span>

[<span data-ttu-id="47af8-132">Yeni-azlı bir</span><span class="sxs-lookup"><span data-stu-id="47af8-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="47af8-133">Set-azapsanana</span><span class="sxs-lookup"><span data-stu-id="47af8-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)