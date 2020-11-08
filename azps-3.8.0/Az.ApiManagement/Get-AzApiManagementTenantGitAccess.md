---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: d9b179ab65fa4d081fd0d065d08dab42f8aee810
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098330"
---
# <span data-ttu-id="dfd2b-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="dfd2b-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="dfd2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfd2b-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd2b-103">Bir kiracı için git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="dfd2b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dfd2b-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfd2b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dfd2b-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd2b-106">**Get-AzApiManagementTenantGitAccess** cmdlet 'i kiracının git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="dfd2b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dfd2b-107">EXAMPLES</span></span>

### <span data-ttu-id="dfd2b-108">Örnek 1: kiracı erişimi yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="dfd2b-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="dfd2b-109">Bu komut belirtilen bağlam için git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="dfd2b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dfd2b-110">PARAMETERS</span></span>

### <span data-ttu-id="dfd2b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="dfd2b-111">-Context</span></span>
<span data-ttu-id="dfd2b-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd2b-113">-DefaultProfile</span></span>
<span data-ttu-id="dfd2b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfd2b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd2b-115">CommonParameters</span></span>
<span data-ttu-id="dfd2b-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd2b-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd2b-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dfd2b-118">INPUTS</span></span>

### <span data-ttu-id="dfd2b-119">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="dfd2b-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="dfd2b-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dfd2b-120">OUTPUTS</span></span>

### <span data-ttu-id="dfd2b-121">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="dfd2b-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="dfd2b-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dfd2b-122">NOTES</span></span>

## <span data-ttu-id="dfd2b-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dfd2b-123">RELATED LINKS</span></span>
