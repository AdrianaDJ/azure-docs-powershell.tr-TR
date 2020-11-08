---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278628"
---
# <span data-ttu-id="d315a-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="d315a-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="d315a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d315a-102">SYNOPSIS</span></span>
<span data-ttu-id="d315a-103">Projeyi geçir 'i silin.</span><span class="sxs-lookup"><span data-stu-id="d315a-103">Delete the migrate project.</span></span>
<span data-ttu-id="d315a-104">Var olmayan projenin silinmesi işlem değildir.</span><span class="sxs-lookup"><span data-stu-id="d315a-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="d315a-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d315a-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d315a-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="d315a-106">DESCRIPTION</span></span>
<span data-ttu-id="d315a-107">Projeyi geçir 'i silin.</span><span class="sxs-lookup"><span data-stu-id="d315a-107">Delete the migrate project.</span></span>
<span data-ttu-id="d315a-108">Var olmayan projenin silinmesi işlem değildir.</span><span class="sxs-lookup"><span data-stu-id="d315a-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="d315a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d315a-109">EXAMPLES</span></span>

### <span data-ttu-id="d315a-110">Örnek 1: Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d315a-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="d315a-111">Projeyi geçir 'i silin.</span><span class="sxs-lookup"><span data-stu-id="d315a-111">Delete the migrate project.</span></span>
<span data-ttu-id="d315a-112">Var olmayan projenin silinmesi işlem değildir.</span><span class="sxs-lookup"><span data-stu-id="d315a-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="d315a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d315a-113">PARAMETERS</span></span>

### <span data-ttu-id="d315a-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="d315a-114">-AcceptLanguage</span></span>
<span data-ttu-id="d315a-115">Standart istek üst bilgisi.</span><span class="sxs-lookup"><span data-stu-id="d315a-115">Standard request header.</span></span>
<span data-ttu-id="d315a-116">Hizmet tarafından, uygun dilde istemciye yanıt vermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d315a-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="d315a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d315a-117">-DefaultProfile</span></span>
<span data-ttu-id="d315a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d315a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d315a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d315a-119">-Name</span></span>
<span data-ttu-id="d315a-120">Azure geçiş projesi adı.</span><span class="sxs-lookup"><span data-stu-id="d315a-120">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d315a-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d315a-121">-PassThru</span></span>
<span data-ttu-id="d315a-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="d315a-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d315a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d315a-123">-ResourceGroupName</span></span>
<span data-ttu-id="d315a-124">Project 'in parçası olduğu Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d315a-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="d315a-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d315a-125">-SubscriptionId</span></span>
<span data-ttu-id="d315a-126">Yükseltme projesinin oluşturulduğu Azure abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="d315a-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="d315a-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="d315a-127">-Confirm</span></span>
<span data-ttu-id="d315a-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d315a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d315a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d315a-129">-WhatIf</span></span>
<span data-ttu-id="d315a-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d315a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d315a-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d315a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d315a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d315a-132">CommonParameters</span></span>
<span data-ttu-id="d315a-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d315a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d315a-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d315a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d315a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d315a-135">INPUTS</span></span>

## <span data-ttu-id="d315a-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d315a-136">OUTPUTS</span></span>

### <span data-ttu-id="d315a-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d315a-137">System.Boolean</span></span>

## <span data-ttu-id="d315a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d315a-138">NOTES</span></span>

<span data-ttu-id="d315a-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d315a-139">ALIASES</span></span>

## <span data-ttu-id="d315a-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d315a-140">RELATED LINKS</span></span>

