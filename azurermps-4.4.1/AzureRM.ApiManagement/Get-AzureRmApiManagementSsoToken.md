---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: 7ca683fc8b4c84a31a651982e5b605d3c29123a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762078"
---
# <span data-ttu-id="80e22-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="80e22-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="80e22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80e22-102">SYNOPSIS</span></span>
<span data-ttu-id="80e22-103">Bir API yönetim hizmetinin dağıtılmış yönetim portalına SSO belirteci içeren bir bağlantı alır.</span><span class="sxs-lookup"><span data-stu-id="80e22-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80e22-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80e22-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80e22-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="80e22-105">DESCRIPTION</span></span>
<span data-ttu-id="80e22-106">**Get-Azurermapsananagementssotoken** CMDLET 'ı API yönetim hizmetinin dağıtılmış yönetim portalına çoklu oturum açma (SSO) belirteci içeren bir bağlantı (URL) döndürür.</span><span class="sxs-lookup"><span data-stu-id="80e22-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="80e22-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80e22-107">EXAMPLES</span></span>

### <span data-ttu-id="80e22-108">Örnek 1: bir API yönetim hizmetinin SSO belirtecini alma</span><span class="sxs-lookup"><span data-stu-id="80e22-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="80e22-109">Bu komut, bir API yönetim hizmetinin SSO belirtecini alır.</span><span class="sxs-lookup"><span data-stu-id="80e22-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="80e22-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80e22-110">PARAMETERS</span></span>

### <span data-ttu-id="80e22-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="80e22-111">-Name</span></span>
<span data-ttu-id="80e22-112">API yönetim örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80e22-112">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="80e22-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80e22-113">-ResourceGroupName</span></span>
<span data-ttu-id="80e22-114">API yönetiminin altında bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80e22-114">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="80e22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80e22-115">-DefaultProfile</span></span>
<span data-ttu-id="80e22-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="80e22-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80e22-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e22-117">CommonParameters</span></span>
<span data-ttu-id="80e22-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80e22-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e22-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80e22-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e22-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80e22-120">INPUTS</span></span>

## <span data-ttu-id="80e22-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80e22-121">OUTPUTS</span></span>

### <span data-ttu-id="80e22-122">System. String</span><span class="sxs-lookup"><span data-stu-id="80e22-122">System.String</span></span>

## <span data-ttu-id="80e22-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80e22-123">NOTES</span></span>

## <span data-ttu-id="80e22-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80e22-124">RELATED LINKS</span></span>

[<span data-ttu-id="80e22-125">Get-azurermapı</span><span class="sxs-lookup"><span data-stu-id="80e22-125">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

