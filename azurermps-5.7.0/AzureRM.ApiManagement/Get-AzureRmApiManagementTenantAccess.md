---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 64f341398ff20f3eddf67c88c51a93125904d566
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589923"
---
# <span data-ttu-id="b3ff9-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="b3ff9-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="b3ff9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ff9-103">Kiracının erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="b3ff9-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3ff9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3ff9-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3ff9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3ff9-105">DESCRIPTION</span></span>
<span data-ttu-id="b3ff9-106">**Get-AzureRmApiManagementTenantAccess** cmdlet 'i kiracının kiracı erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="b3ff9-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="b3ff9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3ff9-107">EXAMPLES</span></span>

### <span data-ttu-id="b3ff9-108">Örnek 1: kiracı erişimi yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="b3ff9-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $apimContext 
```

<span data-ttu-id="b3ff9-109">Bu komut, belirtilen bağlam için kiracı erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="b3ff9-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="b3ff9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3ff9-110">PARAMETERS</span></span>

### <span data-ttu-id="b3ff9-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b3ff9-111">-Context</span></span>
<span data-ttu-id="b3ff9-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ff9-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b3ff9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ff9-113">-DefaultProfile</span></span>
<span data-ttu-id="b3ff9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3ff9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b3ff9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ff9-115">CommonParameters</span></span>
<span data-ttu-id="b3ff9-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3ff9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ff9-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3ff9-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ff9-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3ff9-118">INPUTS</span></span>

### <span data-ttu-id="b3ff9-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b3ff9-119">None</span></span>
<span data-ttu-id="b3ff9-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b3ff9-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b3ff9-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3ff9-121">OUTPUTS</span></span>

### <span data-ttu-id="b3ff9-122">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="b3ff9-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b3ff9-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3ff9-123">NOTES</span></span>

## <span data-ttu-id="b3ff9-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3ff9-124">RELATED LINKS</span></span>

[<span data-ttu-id="b3ff9-125">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="b3ff9-125">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)


