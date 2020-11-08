---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: fd9e4cec821b08c9ac2bbd5cd2ac43e5e5b114ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098382"
---
# <span data-ttu-id="804ea-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="804ea-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="804ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="804ea-102">SYNOPSIS</span></span>
<span data-ttu-id="804ea-103">Bir üründen API 'YI kaldırır.</span><span class="sxs-lookup"><span data-stu-id="804ea-103">Removes an API from a product.</span></span>

## <span data-ttu-id="804ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="804ea-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="804ea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="804ea-105">DESCRIPTION</span></span>
<span data-ttu-id="804ea-106">**Remove-Azapsananagementapifromproduct** cmdlet 'i, bir üründen Azure API yönetim API 'sini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="804ea-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="804ea-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="804ea-107">EXAMPLES</span></span>

### <span data-ttu-id="804ea-108">Örnek 1: bir üründen API 'YI kaldırma</span><span class="sxs-lookup"><span data-stu-id="804ea-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="804ea-109">Bu komut belirtilen API 'YI üründen kaldırır.</span><span class="sxs-lookup"><span data-stu-id="804ea-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="804ea-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="804ea-110">PARAMETERS</span></span>

### <span data-ttu-id="804ea-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="804ea-111">-ApiId</span></span>
<span data-ttu-id="804ea-112">Üründen kaldırılacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="804ea-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="804ea-113">-Context</span><span class="sxs-lookup"><span data-stu-id="804ea-113">-Context</span></span>
<span data-ttu-id="804ea-114">**Psapsananabir Gementcontext** belirtir.</span><span class="sxs-lookup"><span data-stu-id="804ea-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="804ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="804ea-115">-DefaultProfile</span></span>
<span data-ttu-id="804ea-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="804ea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="804ea-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="804ea-117">-PassThru</span></span>
<span data-ttu-id="804ea-118">Bu cmdlet 'in başarılı olduğu bir $True değerini (veya $False) döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="804ea-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="804ea-119">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="804ea-119">-ProductId</span></span>
<span data-ttu-id="804ea-120">API 'nin kaldırılacağı ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="804ea-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="804ea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="804ea-121">CommonParameters</span></span>
<span data-ttu-id="804ea-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="804ea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="804ea-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="804ea-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="804ea-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="804ea-124">INPUTS</span></span>

### <span data-ttu-id="804ea-125">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="804ea-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="804ea-126">System. String</span><span class="sxs-lookup"><span data-stu-id="804ea-126">System.String</span></span>

### <span data-ttu-id="804ea-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="804ea-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="804ea-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="804ea-128">OUTPUTS</span></span>

### <span data-ttu-id="804ea-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="804ea-129">System.Boolean</span></span>

## <span data-ttu-id="804ea-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="804ea-130">NOTES</span></span>

## <span data-ttu-id="804ea-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="804ea-131">RELATED LINKS</span></span>

[<span data-ttu-id="804ea-132">Add-Azapsananagementapitoproduct</span><span class="sxs-lookup"><span data-stu-id="804ea-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


