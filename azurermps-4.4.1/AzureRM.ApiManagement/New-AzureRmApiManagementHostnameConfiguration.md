---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 1b34903f402f7e8d432d16087f1e32fc7b7da3e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591225"
---
# <span data-ttu-id="72be9-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="72be9-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="72be9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72be9-102">SYNOPSIS</span></span>
<span data-ttu-id="72be9-103">PsApiManagementHostnameConfiguration örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="72be9-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72be9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72be9-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72be9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72be9-105">DESCRIPTION</span></span>
<span data-ttu-id="72be9-106">**Yeni-Azurermapsananagementhostnameconfiguration** cmdlet 'ı, **Psapimanagementhostnameconfiguration** örneğini oluşturan bir yardımcı komuttur.</span><span class="sxs-lookup"><span data-stu-id="72be9-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="72be9-107">Bu komut Set-AzureRmApiManagementHostnames cmdlet 'le kullanılır.</span><span class="sxs-lookup"><span data-stu-id="72be9-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="72be9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72be9-108">EXAMPLES</span></span>

### <span data-ttu-id="72be9-109">Örnek 1: PsApiManagementHostnameConfiguration örneği oluşturma ve başlatma</span><span class="sxs-lookup"><span data-stu-id="72be9-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="72be9-110">Bu komut bir **Psapsananagementhostnameconfiguration** örneği oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="72be9-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="72be9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72be9-111">PARAMETERS</span></span>

### <span data-ttu-id="72be9-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="72be9-112">-CertificateThumbprint</span></span>
<span data-ttu-id="72be9-113">Sertifika parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72be9-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="72be9-114">Sertifikanın öncelikle Import-AzureRmApiManagementHostnameCertificate cmdlet 'i ile içeri aktarılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="72be9-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

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

### <span data-ttu-id="72be9-115">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="72be9-115">-Hostname</span></span>
<span data-ttu-id="72be9-116">Bu cmdlet 'in **Psapimanagementhostnameconfiguration** örneğini oluşturduğu özel ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72be9-116">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

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

### <span data-ttu-id="72be9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72be9-117">-DefaultProfile</span></span>
<span data-ttu-id="72be9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72be9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72be9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72be9-119">CommonParameters</span></span>
<span data-ttu-id="72be9-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72be9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72be9-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72be9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72be9-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72be9-122">INPUTS</span></span>

## <span data-ttu-id="72be9-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72be9-123">OUTPUTS</span></span>

### <span data-ttu-id="72be9-124">Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementhostnameconfiguration</span><span class="sxs-lookup"><span data-stu-id="72be9-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="72be9-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72be9-125">NOTES</span></span>

## <span data-ttu-id="72be9-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72be9-126">RELATED LINKS</span></span>

[<span data-ttu-id="72be9-127">Import-Azurermapımanagementhostnamecertificate</span><span class="sxs-lookup"><span data-stu-id="72be9-127">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="72be9-128">Set-Azurermapımanagementhostnames</span><span class="sxs-lookup"><span data-stu-id="72be9-128">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


