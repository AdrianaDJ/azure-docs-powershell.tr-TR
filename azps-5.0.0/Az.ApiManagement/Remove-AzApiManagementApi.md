---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 13f5297efc19aa56cc5af55962c072f5ff2a32d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277869"
---
# <span data-ttu-id="bd88c-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bd88c-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="bd88c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd88c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd88c-103">Bir API 'YI kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bd88c-103">Removes an API.</span></span>

## <span data-ttu-id="bd88c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd88c-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd88c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd88c-105">DESCRIPTION</span></span>
<span data-ttu-id="bd88c-106">**Remove-Azapsananagementapı** cmdlet 'i var olan bir API 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bd88c-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="bd88c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd88c-107">EXAMPLES</span></span>

### <span data-ttu-id="bd88c-108">Örnek 1: API 'YI kaldırma</span><span class="sxs-lookup"><span data-stu-id="bd88c-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="bd88c-109">Bu komut belirtilen KIMLIKLE API 'YI kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bd88c-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="bd88c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd88c-110">PARAMETERS</span></span>

### <span data-ttu-id="bd88c-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="bd88c-111">-ApiId</span></span>
<span data-ttu-id="bd88c-112">API kaldırma KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd88c-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="bd88c-113">-Context</span><span class="sxs-lookup"><span data-stu-id="bd88c-113">-Context</span></span>
<span data-ttu-id="bd88c-114">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd88c-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bd88c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd88c-115">-DefaultProfile</span></span>
<span data-ttu-id="bd88c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd88c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd88c-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bd88c-117">-PassThru</span></span>
<span data-ttu-id="bd88c-118">geçiş</span><span class="sxs-lookup"><span data-stu-id="bd88c-118">passthru</span></span>

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

### <span data-ttu-id="bd88c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="bd88c-119">-Confirm</span></span>
<span data-ttu-id="bd88c-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd88c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd88c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd88c-121">-WhatIf</span></span>
<span data-ttu-id="bd88c-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd88c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd88c-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bd88c-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd88c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd88c-124">CommonParameters</span></span>
<span data-ttu-id="bd88c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd88c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd88c-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bd88c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd88c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd88c-127">INPUTS</span></span>

### <span data-ttu-id="bd88c-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="bd88c-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bd88c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bd88c-129">System.String</span></span>

### <span data-ttu-id="bd88c-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bd88c-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bd88c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd88c-131">OUTPUTS</span></span>

### <span data-ttu-id="bd88c-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd88c-132">System.Boolean</span></span>

## <span data-ttu-id="bd88c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd88c-133">NOTES</span></span>

## <span data-ttu-id="bd88c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd88c-134">RELATED LINKS</span></span>

[<span data-ttu-id="bd88c-135">Dışarı aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="bd88c-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="bd88c-136">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="bd88c-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="bd88c-137">İçeri aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="bd88c-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="bd88c-138">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="bd88c-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="bd88c-139">Set-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="bd88c-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


