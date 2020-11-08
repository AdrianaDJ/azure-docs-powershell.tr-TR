---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: f4e2bb2bce0dc01f99b55497ba671999c9c2ab01
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103856"
---
# <span data-ttu-id="65480-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="65480-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="65480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65480-102">SYNOPSIS</span></span>
<span data-ttu-id="65480-103">Bir API yönetim grubu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="65480-103">Configures an API management group.</span></span>

## <span data-ttu-id="65480-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65480-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65480-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="65480-105">DESCRIPTION</span></span>
<span data-ttu-id="65480-106">**Set-Azapsananagementgroup** cmdlet 'ı bir API yönetim grubu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="65480-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="65480-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65480-107">EXAMPLES</span></span>

### <span data-ttu-id="65480-108">Örnek 1: yönetim grubu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="65480-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="65480-109">Bu komut, Group0001 adlı bir yönetim grubunu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="65480-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="65480-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65480-110">PARAMETERS</span></span>

### <span data-ttu-id="65480-111">-Context</span><span class="sxs-lookup"><span data-stu-id="65480-111">-Context</span></span>
<span data-ttu-id="65480-112">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="65480-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="65480-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65480-113">-DefaultProfile</span></span>
<span data-ttu-id="65480-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65480-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65480-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="65480-115">-Description</span></span>
<span data-ttu-id="65480-116">Yönetim grubunun açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65480-116">Specifies the description of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65480-117">-GroupID</span><span class="sxs-lookup"><span data-stu-id="65480-117">-GroupId</span></span>
<span data-ttu-id="65480-118">Yönetim grubunun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65480-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="65480-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="65480-119">-Name</span></span>
<span data-ttu-id="65480-120">Yönetim grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65480-120">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65480-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="65480-121">-PassThru</span></span>
<span data-ttu-id="65480-122">geçiş</span><span class="sxs-lookup"><span data-stu-id="65480-122">passthru</span></span>

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

### <span data-ttu-id="65480-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="65480-123">-Confirm</span></span>
<span data-ttu-id="65480-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65480-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65480-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65480-125">-WhatIf</span></span>
<span data-ttu-id="65480-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65480-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65480-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65480-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65480-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65480-128">CommonParameters</span></span>
<span data-ttu-id="65480-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65480-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65480-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="65480-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65480-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65480-131">INPUTS</span></span>

### <span data-ttu-id="65480-132">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="65480-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="65480-133">System. String</span><span class="sxs-lookup"><span data-stu-id="65480-133">System.String</span></span>

### <span data-ttu-id="65480-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="65480-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="65480-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65480-135">OUTPUTS</span></span>

### <span data-ttu-id="65480-136">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="65480-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="65480-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65480-137">NOTES</span></span>

## <span data-ttu-id="65480-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65480-138">RELATED LINKS</span></span>

[<span data-ttu-id="65480-139">Get-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="65480-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="65480-140">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="65480-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="65480-141">Remove-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="65480-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


