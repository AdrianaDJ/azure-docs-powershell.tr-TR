---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: 34631b2f1ac68e5f58c6269fa473dcf3d9103c7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917807"
---
# <span data-ttu-id="77e44-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="77e44-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="77e44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77e44-102">SYNOPSIS</span></span>
<span data-ttu-id="77e44-103">Bir üründen API 'YI kaldırır.</span><span class="sxs-lookup"><span data-stu-id="77e44-103">Removes an API from a product.</span></span>

## <span data-ttu-id="77e44-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="77e44-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77e44-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="77e44-105">DESCRIPTION</span></span>
<span data-ttu-id="77e44-106">**Remove-Azapsananagementapifromproduct** cmdlet 'i, bir üründen Azure API yönetim API 'sini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="77e44-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="77e44-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="77e44-107">EXAMPLES</span></span>

### <span data-ttu-id="77e44-108">Örnek 1: bir üründen API 'YI kaldırma</span><span class="sxs-lookup"><span data-stu-id="77e44-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="77e44-109">Bu işlem, belirtilen API 'YI üründen kaldırır.</span><span class="sxs-lookup"><span data-stu-id="77e44-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="77e44-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="77e44-110">PARAMETERS</span></span>

### <span data-ttu-id="77e44-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="77e44-111">-ApiId</span></span>
<span data-ttu-id="77e44-112">Üründen kaldırılacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="77e44-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="77e44-113">-Context</span><span class="sxs-lookup"><span data-stu-id="77e44-113">-Context</span></span>
<span data-ttu-id="77e44-114">**Psapsananabir Gementcontext** belirtir.</span><span class="sxs-lookup"><span data-stu-id="77e44-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="77e44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e44-115">-DefaultProfile</span></span>
<span data-ttu-id="77e44-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="77e44-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77e44-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="77e44-117">-PassThru</span></span>
<span data-ttu-id="77e44-118">Bu cmdlet 'in başarılı olduğu bir $True değerini (veya $False) döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="77e44-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="77e44-119">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="77e44-119">-ProductId</span></span>
<span data-ttu-id="77e44-120">API 'nin kaldırılacağı ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="77e44-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="77e44-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e44-121">CommonParameters</span></span>
<span data-ttu-id="77e44-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="77e44-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e44-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77e44-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e44-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="77e44-124">INPUTS</span></span>

### <span data-ttu-id="77e44-125">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="77e44-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="77e44-126">System. String</span><span class="sxs-lookup"><span data-stu-id="77e44-126">System.String</span></span>

### <span data-ttu-id="77e44-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="77e44-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="77e44-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="77e44-128">OUTPUTS</span></span>

### <span data-ttu-id="77e44-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77e44-129">System.Boolean</span></span>

## <span data-ttu-id="77e44-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="77e44-130">NOTES</span></span>

## <span data-ttu-id="77e44-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="77e44-131">RELATED LINKS</span></span>

[<span data-ttu-id="77e44-132">Add-Azapsananagementapitoproduct</span><span class="sxs-lookup"><span data-stu-id="77e44-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


