---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: 1bd1027c0d58f1ee38ca23c28b3021bdc2b95d19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587353"
---
# <span data-ttu-id="7b959-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="7b959-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="7b959-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b959-102">SYNOPSIS</span></span>
<span data-ttu-id="7b959-103">Bir gruba ürün ekler.</span><span class="sxs-lookup"><span data-stu-id="7b959-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b959-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b959-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b959-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b959-105">DESCRIPTION</span></span>
<span data-ttu-id="7b959-106">**Add-Azurermapımanagementproducttogroup** cmdlet 'i mevcut bir gruba ürün ekler.</span><span class="sxs-lookup"><span data-stu-id="7b959-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="7b959-107">Başka bir deyişle, bu cmdlet ürüne bir grup atar.</span><span class="sxs-lookup"><span data-stu-id="7b959-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="7b959-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b959-108">EXAMPLES</span></span>

### <span data-ttu-id="7b959-109">Örnek 1: gruba ürün ekleme</span><span class="sxs-lookup"><span data-stu-id="7b959-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="7b959-110">Bu komut, mevcut bir gruba ürün ekler.</span><span class="sxs-lookup"><span data-stu-id="7b959-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="7b959-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b959-111">PARAMETERS</span></span>

### <span data-ttu-id="7b959-112">-Context</span><span class="sxs-lookup"><span data-stu-id="7b959-112">-Context</span></span>
<span data-ttu-id="7b959-113">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b959-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="7b959-114">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7b959-114">This parameter is required.</span></span>

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

### <span data-ttu-id="7b959-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b959-115">-DefaultProfile</span></span>
<span data-ttu-id="7b959-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7b959-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b959-117">-GroupID</span><span class="sxs-lookup"><span data-stu-id="7b959-117">-GroupId</span></span>
<span data-ttu-id="7b959-118">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b959-118">Specifies the group ID.</span></span>
<span data-ttu-id="7b959-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7b959-119">This parameter is required.</span></span>

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

### <span data-ttu-id="7b959-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7b959-120">-PassThru</span></span>
<span data-ttu-id="7b959-121">geçiş</span><span class="sxs-lookup"><span data-stu-id="7b959-121">passthru</span></span>

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

### <span data-ttu-id="7b959-122">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="7b959-122">-ProductId</span></span>
<span data-ttu-id="7b959-123">Ürün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b959-123">Specifies the product ID.</span></span>
<span data-ttu-id="7b959-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7b959-124">This parameter is required.</span></span>

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

### <span data-ttu-id="7b959-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b959-125">CommonParameters</span></span>
<span data-ttu-id="7b959-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b959-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b959-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b959-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b959-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b959-128">INPUTS</span></span>

### <span data-ttu-id="7b959-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="7b959-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7b959-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7b959-130">System.String</span></span>

### <span data-ttu-id="7b959-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7b959-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7b959-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b959-132">OUTPUTS</span></span>

### <span data-ttu-id="7b959-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b959-133">System.Boolean</span></span>

## <span data-ttu-id="7b959-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b959-134">NOTES</span></span>

## <span data-ttu-id="7b959-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b959-135">RELATED LINKS</span></span>

[<span data-ttu-id="7b959-136">Remove-Azurermapımanagementproductfromgroup</span><span class="sxs-lookup"><span data-stu-id="7b959-136">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


