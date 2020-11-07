---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 89ea2d36e3b3b65c08e6a053d402f9be4966a738
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917779"
---
# <span data-ttu-id="72cac-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="72cac-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="72cac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72cac-102">SYNOPSIS</span></span>
<span data-ttu-id="72cac-103">Var olan bir API yönetim grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72cac-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="72cac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72cac-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72cac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72cac-105">DESCRIPTION</span></span>
<span data-ttu-id="72cac-106">**Remove-Azapsananagementgroup** cmdlet 'i var olan bir API yönetim grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72cac-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="72cac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72cac-107">EXAMPLES</span></span>

### <span data-ttu-id="72cac-108">Örnek 1: var olan bir yönetim grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="72cac-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="72cac-109">Bu komut Group0001 adlı bir yönetim grubunu kaldırır ve kullanıcıya onay istemez.</span><span class="sxs-lookup"><span data-stu-id="72cac-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="72cac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72cac-110">PARAMETERS</span></span>

### <span data-ttu-id="72cac-111">-Context</span><span class="sxs-lookup"><span data-stu-id="72cac-111">-Context</span></span>
<span data-ttu-id="72cac-112">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72cac-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="72cac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72cac-113">-DefaultProfile</span></span>
<span data-ttu-id="72cac-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72cac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72cac-115">-GroupID</span><span class="sxs-lookup"><span data-stu-id="72cac-115">-GroupId</span></span>
<span data-ttu-id="72cac-116">Yönetim grubunun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72cac-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="72cac-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="72cac-117">-PassThru</span></span>
<span data-ttu-id="72cac-118">Bu cmdlet 'in başarılı olduğu bir $True değerini veya $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72cac-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="72cac-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="72cac-119">-Confirm</span></span>
<span data-ttu-id="72cac-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72cac-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72cac-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72cac-121">-WhatIf</span></span>
<span data-ttu-id="72cac-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72cac-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72cac-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72cac-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72cac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72cac-124">CommonParameters</span></span>
<span data-ttu-id="72cac-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72cac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72cac-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72cac-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72cac-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72cac-127">INPUTS</span></span>

### <span data-ttu-id="72cac-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="72cac-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="72cac-129">System. String</span><span class="sxs-lookup"><span data-stu-id="72cac-129">System.String</span></span>

### <span data-ttu-id="72cac-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="72cac-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="72cac-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72cac-131">OUTPUTS</span></span>

### <span data-ttu-id="72cac-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72cac-132">System.Boolean</span></span>

## <span data-ttu-id="72cac-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72cac-133">NOTES</span></span>

## <span data-ttu-id="72cac-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72cac-134">RELATED LINKS</span></span>

[<span data-ttu-id="72cac-135">Get-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="72cac-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="72cac-136">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="72cac-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="72cac-137">Set-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="72cac-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


