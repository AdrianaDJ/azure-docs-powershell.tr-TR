---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 73e1fbee1dd20a9a30260727f693376346c87f0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108544"
---
# <span data-ttu-id="9a184-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9a184-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="9a184-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a184-102">SYNOPSIS</span></span>
<span data-ttu-id="9a184-103">Var olan bir API yönetim grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9a184-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="9a184-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a184-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a184-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a184-105">DESCRIPTION</span></span>
<span data-ttu-id="9a184-106">**Remove-Azapsananagementgroup** cmdlet 'i var olan bir API yönetim grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9a184-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="9a184-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a184-107">EXAMPLES</span></span>

### <span data-ttu-id="9a184-108">Örnek 1: var olan bir yönetim grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="9a184-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="9a184-109">Bu komut Group0001 adlı bir yönetim grubunu kaldırır ve kullanıcıya onay istemez.</span><span class="sxs-lookup"><span data-stu-id="9a184-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="9a184-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a184-110">PARAMETERS</span></span>

### <span data-ttu-id="9a184-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9a184-111">-Context</span></span>
<span data-ttu-id="9a184-112">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a184-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9a184-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a184-113">-DefaultProfile</span></span>
<span data-ttu-id="9a184-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9a184-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a184-115">-GroupID</span><span class="sxs-lookup"><span data-stu-id="9a184-115">-GroupId</span></span>
<span data-ttu-id="9a184-116">Yönetim grubunun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a184-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="9a184-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9a184-117">-PassThru</span></span>
<span data-ttu-id="9a184-118">Bu cmdlet 'in başarılı olduğu bir $True değerini veya $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a184-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="9a184-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="9a184-119">-Confirm</span></span>
<span data-ttu-id="9a184-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9a184-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a184-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a184-121">-WhatIf</span></span>
<span data-ttu-id="9a184-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9a184-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a184-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9a184-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a184-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a184-124">CommonParameters</span></span>
<span data-ttu-id="9a184-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a184-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a184-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9a184-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a184-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a184-127">INPUTS</span></span>

### <span data-ttu-id="9a184-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="9a184-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9a184-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9a184-129">System.String</span></span>

### <span data-ttu-id="9a184-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9a184-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9a184-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a184-131">OUTPUTS</span></span>

### <span data-ttu-id="9a184-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a184-132">System.Boolean</span></span>

## <span data-ttu-id="9a184-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a184-133">NOTES</span></span>

## <span data-ttu-id="9a184-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a184-134">RELATED LINKS</span></span>

[<span data-ttu-id="9a184-135">Get-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="9a184-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="9a184-136">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="9a184-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="9a184-137">Set-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="9a184-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


