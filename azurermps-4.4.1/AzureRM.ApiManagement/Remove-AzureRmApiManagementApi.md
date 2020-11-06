---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: cadae96af05ae11f76d3a8ea0010da4d73161186
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587037"
---
# <span data-ttu-id="a035d-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a035d-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="a035d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a035d-102">SYNOPSIS</span></span>
<span data-ttu-id="a035d-103">Bir API 'YI kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a035d-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a035d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a035d-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a035d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a035d-105">DESCRIPTION</span></span>
<span data-ttu-id="a035d-106">**Remove-Azurermapsananagementapı** cmdlet 'i var olan bir API 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a035d-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="a035d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a035d-107">EXAMPLES</span></span>

### <span data-ttu-id="a035d-108">Örnek 1: API 'YI kaldırma</span><span class="sxs-lookup"><span data-stu-id="a035d-108">Example 1: Remove an API</span></span>
```
PS C:\>Remove-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789"
```

<span data-ttu-id="a035d-109">Bu komut belirtilen KIMLIKLE API 'YI kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a035d-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="a035d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a035d-110">PARAMETERS</span></span>

### <span data-ttu-id="a035d-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="a035d-111">-ApiId</span></span>
<span data-ttu-id="a035d-112">API kaldırma KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a035d-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="a035d-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a035d-113">-Context</span></span>
<span data-ttu-id="a035d-114">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a035d-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a035d-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a035d-115">-PassThru</span></span>
<span data-ttu-id="a035d-116">geçiş</span><span class="sxs-lookup"><span data-stu-id="a035d-116">passthru</span></span>

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

### <span data-ttu-id="a035d-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="a035d-117">-Confirm</span></span>
<span data-ttu-id="a035d-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a035d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a035d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a035d-119">-WhatIf</span></span>
<span data-ttu-id="a035d-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a035d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a035d-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a035d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a035d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a035d-122">-DefaultProfile</span></span>
<span data-ttu-id="a035d-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a035d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a035d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a035d-124">CommonParameters</span></span>
<span data-ttu-id="a035d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a035d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a035d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a035d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a035d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a035d-127">INPUTS</span></span>

## <span data-ttu-id="a035d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a035d-128">OUTPUTS</span></span>

### <span data-ttu-id="a035d-129">Boole</span><span class="sxs-lookup"><span data-stu-id="a035d-129">Boolean</span></span>

## <span data-ttu-id="a035d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a035d-130">NOTES</span></span>

## <span data-ttu-id="a035d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a035d-131">RELATED LINKS</span></span>

[<span data-ttu-id="a035d-132">Dışarı aktarma-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="a035d-132">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="a035d-133">Get-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="a035d-133">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="a035d-134">Import-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="a035d-134">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="a035d-135">Yeni-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="a035d-135">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="a035d-136">Set-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="a035d-136">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


