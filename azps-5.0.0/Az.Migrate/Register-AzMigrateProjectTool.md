---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278633"
---
# <span data-ttu-id="76f05-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="76f05-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="76f05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76f05-102">SYNOPSIS</span></span>
<span data-ttu-id="76f05-103">Projeyi geçir 'e sahip bir aracı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="76f05-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="76f05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76f05-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76f05-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76f05-105">DESCRIPTION</span></span>
<span data-ttu-id="76f05-106">Projeyi geçir 'e sahip bir aracı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="76f05-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="76f05-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76f05-107">EXAMPLES</span></span>

### <span data-ttu-id="76f05-108">Örnek 1: kayıt aracı.</span><span class="sxs-lookup"><span data-stu-id="76f05-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="76f05-109">Projeyi geçir 'e sahip bir aracı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="76f05-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="76f05-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76f05-110">PARAMETERS</span></span>

### <span data-ttu-id="76f05-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="76f05-111">-AcceptLanguage</span></span>
<span data-ttu-id="76f05-112">Standart istek üst bilgisi.</span><span class="sxs-lookup"><span data-stu-id="76f05-112">Standard request header.</span></span>
<span data-ttu-id="76f05-113">Hizmet tarafından, uygun dilde istemciye yanıt vermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="76f05-113">Used by service to respond to client in appropriate language.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f05-114">-DefaultProfile</span></span>
<span data-ttu-id="76f05-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76f05-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f05-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="76f05-116">-MigrateProjectName</span></span>
<span data-ttu-id="76f05-117">Azure geçiş projesi adı.</span><span class="sxs-lookup"><span data-stu-id="76f05-117">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f05-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76f05-118">-ResourceGroupName</span></span>
<span data-ttu-id="76f05-119">Project 'in parçası olduğu Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="76f05-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f05-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="76f05-120">-SubscriptionId</span></span>
<span data-ttu-id="76f05-121">Yükseltme projesinin oluşturulduğu Azure abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="76f05-121">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f05-122">-Araç</span><span class="sxs-lookup"><span data-stu-id="76f05-122">-Tool</span></span>
<span data-ttu-id="76f05-123">Kaydedilecek aracı alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="76f05-123">Gets or sets the tool to be registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f05-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="76f05-124">-Confirm</span></span>
<span data-ttu-id="76f05-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="76f05-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76f05-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76f05-126">-WhatIf</span></span>
<span data-ttu-id="76f05-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="76f05-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76f05-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="76f05-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76f05-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f05-129">CommonParameters</span></span>
<span data-ttu-id="76f05-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76f05-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f05-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="76f05-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f05-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76f05-132">INPUTS</span></span>

## <span data-ttu-id="76f05-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76f05-133">OUTPUTS</span></span>

### <span data-ttu-id="76f05-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76f05-134">System.Boolean</span></span>

## <span data-ttu-id="76f05-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76f05-135">NOTES</span></span>

<span data-ttu-id="76f05-136">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="76f05-136">ALIASES</span></span>

## <span data-ttu-id="76f05-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76f05-137">RELATED LINKS</span></span>

