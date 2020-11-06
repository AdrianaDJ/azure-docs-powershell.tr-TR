---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: b4e1a029eca4e7eda48f44d85292639767eaf845
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592693"
---
# <span data-ttu-id="15a61-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="15a61-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="15a61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15a61-102">SYNOPSIS</span></span>
<span data-ttu-id="15a61-103">Bir gruba ürün ekler.</span><span class="sxs-lookup"><span data-stu-id="15a61-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15a61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15a61-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15a61-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15a61-105">DESCRIPTION</span></span>
<span data-ttu-id="15a61-106">**Add-Azurermapımanagementproducttogroup** cmdlet 'i mevcut bir gruba ürün ekler.</span><span class="sxs-lookup"><span data-stu-id="15a61-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="15a61-107">Başka bir deyişle, bu cmdlet ürüne bir grup atar.</span><span class="sxs-lookup"><span data-stu-id="15a61-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="15a61-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15a61-108">EXAMPLES</span></span>

### <span data-ttu-id="15a61-109">Örnek 1: gruba ürün ekleme</span><span class="sxs-lookup"><span data-stu-id="15a61-109">Example 1: Add a product to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="15a61-110">Bu komut, mevcut bir gruba ürün ekler.</span><span class="sxs-lookup"><span data-stu-id="15a61-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="15a61-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15a61-111">PARAMETERS</span></span>

### <span data-ttu-id="15a61-112">-Context</span><span class="sxs-lookup"><span data-stu-id="15a61-112">-Context</span></span>
<span data-ttu-id="15a61-113">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="15a61-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="15a61-114">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="15a61-114">This parameter is required.</span></span>

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

### <span data-ttu-id="15a61-115">-GroupID</span><span class="sxs-lookup"><span data-stu-id="15a61-115">-GroupId</span></span>
<span data-ttu-id="15a61-116">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="15a61-116">Specifies the group ID.</span></span>
<span data-ttu-id="15a61-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="15a61-117">This parameter is required.</span></span>

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

### <span data-ttu-id="15a61-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="15a61-118">-PassThru</span></span>
<span data-ttu-id="15a61-119">geçiş</span><span class="sxs-lookup"><span data-stu-id="15a61-119">passthru</span></span>

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

### <span data-ttu-id="15a61-120">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="15a61-120">-ProductId</span></span>
<span data-ttu-id="15a61-121">Ürün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="15a61-121">Specifies the product ID.</span></span>
<span data-ttu-id="15a61-122">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="15a61-122">This parameter is required.</span></span>

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

### <span data-ttu-id="15a61-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a61-123">-DefaultProfile</span></span>
<span data-ttu-id="15a61-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15a61-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15a61-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a61-125">CommonParameters</span></span>
<span data-ttu-id="15a61-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15a61-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a61-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a61-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a61-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15a61-128">INPUTS</span></span>

## <span data-ttu-id="15a61-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15a61-129">OUTPUTS</span></span>

### <span data-ttu-id="15a61-130">Boole</span><span class="sxs-lookup"><span data-stu-id="15a61-130">Boolean</span></span>

## <span data-ttu-id="15a61-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15a61-131">NOTES</span></span>

## <span data-ttu-id="15a61-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15a61-132">RELATED LINKS</span></span>

[<span data-ttu-id="15a61-133">Remove-Azurermapımanagementproductfromgroup</span><span class="sxs-lookup"><span data-stu-id="15a61-133">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


