---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 066538db3a763c5a3c6d9de9f621ca2b81552983
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586847"
---
# <span data-ttu-id="95dc7-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="95dc7-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="95dc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="95dc7-103">PsApiManagementHostnameConfiguration örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="95dc7-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95dc7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95dc7-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95dc7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="95dc7-105">DESCRIPTION</span></span>
<span data-ttu-id="95dc7-106">**Yeni-Azurermapsananagementhostnameconfiguration** cmdlet 'ı, **Psapimanagementhostnameconfiguration** örneğini oluşturan bir yardımcı komuttur.</span><span class="sxs-lookup"><span data-stu-id="95dc7-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="95dc7-107">Bu komut Set-AzureRmApiManagementHostnames cmdlet 'le kullanılır.</span><span class="sxs-lookup"><span data-stu-id="95dc7-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="95dc7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95dc7-108">EXAMPLES</span></span>

### <span data-ttu-id="95dc7-109">Örnek 1: PsApiManagementHostnameConfiguration örneği oluşturma ve başlatma</span><span class="sxs-lookup"><span data-stu-id="95dc7-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="95dc7-110">Bu komut bir **Psapsananagementhostnameconfiguration** örneği oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="95dc7-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="95dc7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95dc7-111">PARAMETERS</span></span>

### <span data-ttu-id="95dc7-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="95dc7-112">-CertificateThumbprint</span></span>
<span data-ttu-id="95dc7-113">Sertifika parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="95dc7-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="95dc7-114">Sertifikanın öncelikle Import-AzureRmApiManagementHostnameCertificate cmdlet 'i ile içeri aktarılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="95dc7-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95dc7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95dc7-115">-DefaultProfile</span></span>
<span data-ttu-id="95dc7-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95dc7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="95dc7-117">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="95dc7-117">-Hostname</span></span>
<span data-ttu-id="95dc7-118">Bu cmdlet 'in **Psapimanagementhostnameconfiguration** örneğini oluşturduğu özel ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95dc7-118">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95dc7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95dc7-119">CommonParameters</span></span>
<span data-ttu-id="95dc7-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95dc7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95dc7-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95dc7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95dc7-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95dc7-122">INPUTS</span></span>

### <span data-ttu-id="95dc7-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="95dc7-123">None</span></span>
<span data-ttu-id="95dc7-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="95dc7-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95dc7-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95dc7-125">OUTPUTS</span></span>

### <span data-ttu-id="95dc7-126">Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementhostnameconfiguration</span><span class="sxs-lookup"><span data-stu-id="95dc7-126">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="95dc7-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95dc7-127">NOTES</span></span>

## <span data-ttu-id="95dc7-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95dc7-128">RELATED LINKS</span></span>

[<span data-ttu-id="95dc7-129">Import-Azurermapımanagementhostnamecertificate</span><span class="sxs-lookup"><span data-stu-id="95dc7-129">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="95dc7-130">Set-Azurermapımanagementhostnames</span><span class="sxs-lookup"><span data-stu-id="95dc7-130">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


