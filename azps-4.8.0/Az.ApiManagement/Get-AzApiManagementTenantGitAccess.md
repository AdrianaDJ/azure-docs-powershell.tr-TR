---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 0a3d2aeb8c90377f9c7e81ef6a25cef49780e410
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109258"
---
# <span data-ttu-id="223fb-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="223fb-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="223fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="223fb-102">SYNOPSIS</span></span>
<span data-ttu-id="223fb-103">Bir kiracı için git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="223fb-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="223fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="223fb-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="223fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="223fb-105">DESCRIPTION</span></span>
<span data-ttu-id="223fb-106">**Get-AzApiManagementTenantGitAccess** cmdlet 'i kiracının git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="223fb-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="223fb-107">Anahtarlar sonuç ayrıntılarına dahil olmaz.</span><span class="sxs-lookup"><span data-stu-id="223fb-107">Keys will not be included into result details.</span></span> <span data-ttu-id="223fb-108">İstemci gizliliğini almak için **Get-Azapsananagementtenantgitaccesssecret** seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="223fb-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="223fb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="223fb-109">EXAMPLES</span></span>

### <span data-ttu-id="223fb-110">Örnek 1: kiracı erişimi yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="223fb-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="223fb-111">Bu komut belirtilen bağlam için git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="223fb-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="223fb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="223fb-112">PARAMETERS</span></span>

### <span data-ttu-id="223fb-113">-Context</span><span class="sxs-lookup"><span data-stu-id="223fb-113">-Context</span></span>
<span data-ttu-id="223fb-114">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="223fb-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="223fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="223fb-115">-DefaultProfile</span></span>
<span data-ttu-id="223fb-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="223fb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="223fb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="223fb-117">CommonParameters</span></span>
<span data-ttu-id="223fb-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="223fb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="223fb-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="223fb-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="223fb-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="223fb-120">INPUTS</span></span>

### <span data-ttu-id="223fb-121">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="223fb-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="223fb-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="223fb-122">OUTPUTS</span></span>

### <span data-ttu-id="223fb-123">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="223fb-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="223fb-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="223fb-124">NOTES</span></span>

## <span data-ttu-id="223fb-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="223fb-125">RELATED LINKS</span></span>
