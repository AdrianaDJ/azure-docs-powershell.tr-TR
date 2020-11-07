---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: 2418ec3f5e9570046c37c76bdaef8f853ff819b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751143"
---
# <span data-ttu-id="baef4-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="baef4-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="baef4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baef4-102">SYNOPSIS</span></span>
<span data-ttu-id="baef4-103">Kiracının erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="baef4-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="baef4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="baef4-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="baef4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="baef4-105">DESCRIPTION</span></span>
<span data-ttu-id="baef4-106">**Get-AzApiManagementTenantAccess** cmdlet 'i kiracının kiracı erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="baef4-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="baef4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="baef4-107">EXAMPLES</span></span>

### <span data-ttu-id="baef4-108">Örnek 1: kiracı erişimi yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="baef4-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="baef4-109">Bu komut, belirtilen bağlam için kiracı erişim yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="baef4-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="baef4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="baef4-110">PARAMETERS</span></span>

### <span data-ttu-id="baef4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="baef4-111">-Context</span></span>
<span data-ttu-id="baef4-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="baef4-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="baef4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baef4-113">-DefaultProfile</span></span>
<span data-ttu-id="baef4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="baef4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baef4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baef4-115">CommonParameters</span></span>
<span data-ttu-id="baef4-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="baef4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baef4-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baef4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baef4-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="baef4-118">INPUTS</span></span>

### <span data-ttu-id="baef4-119">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="baef4-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="baef4-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="baef4-120">OUTPUTS</span></span>

### <span data-ttu-id="baef4-121">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="baef4-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="baef4-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="baef4-122">NOTES</span></span>

## <span data-ttu-id="baef4-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="baef4-123">RELATED LINKS</span></span>

[<span data-ttu-id="baef4-124">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="baef4-124">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


