---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 69f643f4d2e66f0b5af61a6362e59386b2f79078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593855"
---
# <span data-ttu-id="3a910-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="3a910-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="3a910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a910-102">SYNOPSIS</span></span>
<span data-ttu-id="3a910-103">Bir kiracı için git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="3a910-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a910-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a910-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a910-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a910-105">DESCRIPTION</span></span>
<span data-ttu-id="3a910-106">**Get-AzureRmApiManagementTenantGitAccess** cmdlet 'i kiracının git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="3a910-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="3a910-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a910-107">EXAMPLES</span></span>

### <span data-ttu-id="3a910-108">Örnek 1: kiracı erişimi yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="3a910-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $ApimContext
```

<span data-ttu-id="3a910-109">Bu komut belirtilen bağlam için git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="3a910-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="3a910-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a910-110">PARAMETERS</span></span>

### <span data-ttu-id="3a910-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3a910-111">-Context</span></span>
<span data-ttu-id="3a910-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a910-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3a910-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a910-113">-DefaultProfile</span></span>
<span data-ttu-id="3a910-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a910-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a910-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a910-115">CommonParameters</span></span>
<span data-ttu-id="3a910-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a910-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a910-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a910-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a910-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a910-118">INPUTS</span></span>

## <span data-ttu-id="3a910-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a910-119">OUTPUTS</span></span>

### <span data-ttu-id="3a910-120">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="3a910-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="3a910-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a910-121">NOTES</span></span>

## <span data-ttu-id="3a910-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a910-122">RELATED LINKS</span></span>

