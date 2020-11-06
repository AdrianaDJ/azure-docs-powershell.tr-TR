---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: defd5c046427115e44783d6b34ea7b034edc8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587344"
---
# <span data-ttu-id="82067-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="82067-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="82067-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82067-102">SYNOPSIS</span></span>
<span data-ttu-id="82067-103">PsApiManagementHostnameConfiguration örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82067-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82067-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82067-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82067-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="82067-105">DESCRIPTION</span></span>
<span data-ttu-id="82067-106">**Yeni-Azurermapsananagementhostnameconfiguration** cmdlet 'ı, **Psapimanagementhostnameconfiguration** örneğini oluşturan bir yardımcı komuttur.</span><span class="sxs-lookup"><span data-stu-id="82067-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="82067-107">Bu komut Set-AzureRmApiManagementHostnames cmdlet 'le kullanılır.</span><span class="sxs-lookup"><span data-stu-id="82067-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="82067-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82067-108">EXAMPLES</span></span>

### <span data-ttu-id="82067-109">Örnek 1: PsApiManagementHostnameConfiguration örneği oluşturma ve başlatma</span><span class="sxs-lookup"><span data-stu-id="82067-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="82067-110">Bu komut bir **Psapsananagementhostnameconfiguration** örneği oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="82067-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="82067-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82067-111">PARAMETERS</span></span>

### <span data-ttu-id="82067-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="82067-112">-CertificateThumbprint</span></span>
<span data-ttu-id="82067-113">Sertifika parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="82067-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="82067-114">Sertifikanın öncelikle Import-AzureRmApiManagementHostnameCertificate cmdlet 'i ile içeri aktarılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="82067-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82067-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82067-115">-DefaultProfile</span></span>
<span data-ttu-id="82067-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82067-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82067-117">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="82067-117">-Hostname</span></span>
<span data-ttu-id="82067-118">Bu cmdlet 'in **Psapimanagementhostnameconfiguration** örneğini oluşturduğu özel ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82067-118">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82067-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82067-119">CommonParameters</span></span>
<span data-ttu-id="82067-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82067-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82067-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82067-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82067-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82067-122">INPUTS</span></span>

### <span data-ttu-id="82067-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="82067-123">None</span></span>

## <span data-ttu-id="82067-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82067-124">OUTPUTS</span></span>

### <span data-ttu-id="82067-125">Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementhostnameconfiguration</span><span class="sxs-lookup"><span data-stu-id="82067-125">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="82067-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82067-126">NOTES</span></span>

## <span data-ttu-id="82067-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82067-127">RELATED LINKS</span></span>

[<span data-ttu-id="82067-128">Import-Azurermapımanagementhostnamecertificate</span><span class="sxs-lookup"><span data-stu-id="82067-128">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="82067-129">Set-Azurermapımanagementhostnames</span><span class="sxs-lookup"><span data-stu-id="82067-129">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


