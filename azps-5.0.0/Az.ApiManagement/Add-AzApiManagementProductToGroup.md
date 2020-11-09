---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321974"
---
# <span data-ttu-id="c48e8-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="c48e8-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="c48e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c48e8-102">SYNOPSIS</span></span>
<span data-ttu-id="c48e8-103">Bir gruba ürün ekler.</span><span class="sxs-lookup"><span data-stu-id="c48e8-103">Adds a product to a group.</span></span>

## <span data-ttu-id="c48e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c48e8-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c48e8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c48e8-105">DESCRIPTION</span></span>
<span data-ttu-id="c48e8-106">**Add-Azapsananagementproducttogroup** cmdlet 'i mevcut bir gruba ürün ekler.</span><span class="sxs-lookup"><span data-stu-id="c48e8-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="c48e8-107">Başka bir deyişle, bu cmdlet ürüne bir grup atar.</span><span class="sxs-lookup"><span data-stu-id="c48e8-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="c48e8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c48e8-108">EXAMPLES</span></span>

### <span data-ttu-id="c48e8-109">Örnek 1: gruba ürün ekleme</span><span class="sxs-lookup"><span data-stu-id="c48e8-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="c48e8-110">Bu komut, mevcut bir gruba ürün ekler.</span><span class="sxs-lookup"><span data-stu-id="c48e8-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="c48e8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c48e8-111">PARAMETERS</span></span>

### <span data-ttu-id="c48e8-112">-Context</span><span class="sxs-lookup"><span data-stu-id="c48e8-112">-Context</span></span>
<span data-ttu-id="c48e8-113">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c48e8-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="c48e8-114">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c48e8-114">This parameter is required.</span></span>

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

### <span data-ttu-id="c48e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48e8-115">-DefaultProfile</span></span>
<span data-ttu-id="c48e8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c48e8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c48e8-117">-GroupID</span><span class="sxs-lookup"><span data-stu-id="c48e8-117">-GroupId</span></span>
<span data-ttu-id="c48e8-118">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c48e8-118">Specifies the group ID.</span></span>
<span data-ttu-id="c48e8-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c48e8-119">This parameter is required.</span></span>

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

### <span data-ttu-id="c48e8-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c48e8-120">-PassThru</span></span>
<span data-ttu-id="c48e8-121">geçiş</span><span class="sxs-lookup"><span data-stu-id="c48e8-121">passthru</span></span>

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

### <span data-ttu-id="c48e8-122">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="c48e8-122">-ProductId</span></span>
<span data-ttu-id="c48e8-123">Ürün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c48e8-123">Specifies the product ID.</span></span>
<span data-ttu-id="c48e8-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c48e8-124">This parameter is required.</span></span>

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

### <span data-ttu-id="c48e8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48e8-125">CommonParameters</span></span>
<span data-ttu-id="c48e8-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c48e8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48e8-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c48e8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48e8-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c48e8-128">INPUTS</span></span>

### <span data-ttu-id="c48e8-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="c48e8-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c48e8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c48e8-130">System.String</span></span>

### <span data-ttu-id="c48e8-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c48e8-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c48e8-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c48e8-132">OUTPUTS</span></span>

### <span data-ttu-id="c48e8-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c48e8-133">System.Boolean</span></span>

## <span data-ttu-id="c48e8-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c48e8-134">NOTES</span></span>

## <span data-ttu-id="c48e8-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c48e8-135">RELATED LINKS</span></span>

[<span data-ttu-id="c48e8-136">Remove-Azapsananagementproductfromgroup</span><span class="sxs-lookup"><span data-stu-id="c48e8-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


