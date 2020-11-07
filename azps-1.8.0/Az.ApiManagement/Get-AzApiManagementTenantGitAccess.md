---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 2fe14349b179634bf93050840271d4d4b6905b3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751142"
---
# <span data-ttu-id="8fbdc-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="8fbdc-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="8fbdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fbdc-102">SYNOPSIS</span></span>
<span data-ttu-id="8fbdc-103">Bir kiracı için git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="8fbdc-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="8fbdc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8fbdc-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8fbdc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8fbdc-105">DESCRIPTION</span></span>
<span data-ttu-id="8fbdc-106">**Get-AzApiManagementTenantGitAccess** cmdlet 'i kiracının git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="8fbdc-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="8fbdc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8fbdc-107">EXAMPLES</span></span>

### <span data-ttu-id="8fbdc-108">Örnek 1: kiracı erişimi yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="8fbdc-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

<span data-ttu-id="8fbdc-109">Bu komut belirtilen bağlam için git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="8fbdc-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="8fbdc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8fbdc-110">PARAMETERS</span></span>

### <span data-ttu-id="8fbdc-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8fbdc-111">-Context</span></span>
<span data-ttu-id="8fbdc-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fbdc-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8fbdc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fbdc-113">-DefaultProfile</span></span>
<span data-ttu-id="8fbdc-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8fbdc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fbdc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fbdc-115">CommonParameters</span></span>
<span data-ttu-id="8fbdc-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8fbdc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fbdc-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fbdc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fbdc-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8fbdc-118">INPUTS</span></span>

### <span data-ttu-id="8fbdc-119">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="8fbdc-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="8fbdc-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8fbdc-120">OUTPUTS</span></span>

### <span data-ttu-id="8fbdc-121">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="8fbdc-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="8fbdc-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8fbdc-122">NOTES</span></span>

## <span data-ttu-id="8fbdc-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8fbdc-123">RELATED LINKS</span></span>