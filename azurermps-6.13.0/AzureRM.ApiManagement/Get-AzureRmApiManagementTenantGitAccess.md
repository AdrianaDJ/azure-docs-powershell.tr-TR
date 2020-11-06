---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 643877de4ab2b9107459beaa7acb276072a249ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589618"
---
# <span data-ttu-id="902b4-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="902b4-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="902b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="902b4-102">SYNOPSIS</span></span>
<span data-ttu-id="902b4-103">Bir kiracı için git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="902b4-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="902b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="902b4-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="902b4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="902b4-105">DESCRIPTION</span></span>
<span data-ttu-id="902b4-106">**Get-AzureRmApiManagementTenantGitAccess** cmdlet 'i kiracının git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="902b4-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="902b4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="902b4-107">EXAMPLES</span></span>

### <span data-ttu-id="902b4-108">Örnek 1: kiracı erişimi yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="902b4-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $apimContext
```

<span data-ttu-id="902b4-109">Bu komut belirtilen bağlam için git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="902b4-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="902b4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="902b4-110">PARAMETERS</span></span>

### <span data-ttu-id="902b4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="902b4-111">-Context</span></span>
<span data-ttu-id="902b4-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="902b4-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="902b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="902b4-113">-DefaultProfile</span></span>
<span data-ttu-id="902b4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="902b4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="902b4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="902b4-115">CommonParameters</span></span>
<span data-ttu-id="902b4-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="902b4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="902b4-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="902b4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="902b4-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="902b4-118">INPUTS</span></span>

### <span data-ttu-id="902b4-119">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="902b4-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="902b4-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="902b4-120">OUTPUTS</span></span>

### <span data-ttu-id="902b4-121">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="902b4-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="902b4-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="902b4-122">NOTES</span></span>

## <span data-ttu-id="902b4-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="902b4-123">RELATED LINKS</span></span>
