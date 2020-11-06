---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 28b27ee7a2e24b425d5ffa93be4d1f3513a31c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589919"
---
# <span data-ttu-id="1760f-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="1760f-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="1760f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1760f-102">SYNOPSIS</span></span>
<span data-ttu-id="1760f-103">Bir kiracı için git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="1760f-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1760f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1760f-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1760f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1760f-105">DESCRIPTION</span></span>
<span data-ttu-id="1760f-106">**Get-AzureRmApiManagementTenantGitAccess** cmdlet 'i kiracının git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="1760f-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="1760f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1760f-107">EXAMPLES</span></span>

### <span data-ttu-id="1760f-108">Örnek 1: kiracı erişimi yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="1760f-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $apimContext 
```

<span data-ttu-id="1760f-109">Bu komut belirtilen bağlam için git erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="1760f-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="1760f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1760f-110">PARAMETERS</span></span>

### <span data-ttu-id="1760f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1760f-111">-Context</span></span>
<span data-ttu-id="1760f-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1760f-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1760f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1760f-113">-DefaultProfile</span></span>
<span data-ttu-id="1760f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1760f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1760f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1760f-115">CommonParameters</span></span>
<span data-ttu-id="1760f-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1760f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1760f-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1760f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1760f-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1760f-118">INPUTS</span></span>

### <span data-ttu-id="1760f-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1760f-119">None</span></span>
<span data-ttu-id="1760f-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1760f-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1760f-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1760f-121">OUTPUTS</span></span>

### <span data-ttu-id="1760f-122">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="1760f-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="1760f-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1760f-123">NOTES</span></span>

## <span data-ttu-id="1760f-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1760f-124">RELATED LINKS</span></span>

