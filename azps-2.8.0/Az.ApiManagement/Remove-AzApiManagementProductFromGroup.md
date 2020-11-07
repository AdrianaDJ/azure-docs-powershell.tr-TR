---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: 51f4caf679cf2440165e1808c152162d1f272d05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753448"
---
# <span data-ttu-id="bc57b-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="bc57b-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="bc57b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc57b-102">SYNOPSIS</span></span>
<span data-ttu-id="bc57b-103">Bir gruptan bir ürünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc57b-103">Removes a product from a group.</span></span>

## <span data-ttu-id="bc57b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc57b-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc57b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc57b-105">DESCRIPTION</span></span>
<span data-ttu-id="bc57b-106">**Remove-Azapsananagementproductfromgroup** cmdlet 'i mevcut bir gruptan bir ürünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc57b-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="bc57b-107">Başka bir deyişle, bu cmdlet bir üründen grup atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc57b-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="bc57b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc57b-108">EXAMPLES</span></span>

### <span data-ttu-id="bc57b-109">Örnek 1: gruptan ürün kaldırma</span><span class="sxs-lookup"><span data-stu-id="bc57b-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="bc57b-110">Bu komut, mevcut bir gruptan bir ürünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc57b-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="bc57b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc57b-111">PARAMETERS</span></span>

### <span data-ttu-id="bc57b-112">-Context</span><span class="sxs-lookup"><span data-stu-id="bc57b-112">-Context</span></span>
<span data-ttu-id="bc57b-113">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc57b-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="bc57b-114">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="bc57b-114">This parameter is required.</span></span>

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

### <span data-ttu-id="bc57b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc57b-115">-DefaultProfile</span></span>
<span data-ttu-id="bc57b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc57b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc57b-117">-GroupID</span><span class="sxs-lookup"><span data-stu-id="bc57b-117">-GroupId</span></span>
<span data-ttu-id="bc57b-118">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc57b-118">Specifies the group ID.</span></span>
<span data-ttu-id="bc57b-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="bc57b-119">This parameter is required.</span></span>

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

### <span data-ttu-id="bc57b-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bc57b-120">-PassThru</span></span>
<span data-ttu-id="bc57b-121">Bu cmdlet 'in $True değeri (başarılı olursa) veya $False olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc57b-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="bc57b-122">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="bc57b-122">-ProductId</span></span>
<span data-ttu-id="bc57b-123">Ürün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc57b-123">Specifies the product ID.</span></span>
<span data-ttu-id="bc57b-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="bc57b-124">This parameter is required.</span></span>

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

### <span data-ttu-id="bc57b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc57b-125">CommonParameters</span></span>
<span data-ttu-id="bc57b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc57b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc57b-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bc57b-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc57b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc57b-128">INPUTS</span></span>

### <span data-ttu-id="bc57b-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="bc57b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bc57b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bc57b-130">System.String</span></span>

### <span data-ttu-id="bc57b-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bc57b-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bc57b-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc57b-132">OUTPUTS</span></span>

### <span data-ttu-id="bc57b-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc57b-133">System.Boolean</span></span>

## <span data-ttu-id="bc57b-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc57b-134">NOTES</span></span>

## <span data-ttu-id="bc57b-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc57b-135">RELATED LINKS</span></span>

[<span data-ttu-id="bc57b-136">Add-Azapsananagementproducttogroup</span><span class="sxs-lookup"><span data-stu-id="bc57b-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)

