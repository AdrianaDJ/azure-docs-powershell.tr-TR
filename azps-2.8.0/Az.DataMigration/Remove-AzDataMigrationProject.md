---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: 53dc4841dbbdcb7f3d855630b69a94320b4dfeff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752238"
---
# <span data-ttu-id="a31b7-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="a31b7-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="a31b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a31b7-102">SYNOPSIS</span></span>
<span data-ttu-id="a31b7-103">Azure veritabanı geçiş hizmeti projesini Azure 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a31b7-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="a31b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a31b7-104">SYNTAX</span></span>

### <span data-ttu-id="a31b7-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a31b7-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a31b7-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="a31b7-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a31b7-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a31b7-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a31b7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a31b7-108">DESCRIPTION</span></span>
<span data-ttu-id="a31b7-109">Remove-AzDataMigrationProject cmdlet 'i Azure 'dan Azure veritabanı geçiş hizmeti projesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a31b7-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="a31b7-110">DeleteRunningTask parametresi sağlanırken, kaldırılmakta olan projeyle ilişkili tüm Azure veritabanı yükseltme hizmeti görevleri kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a31b7-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="a31b7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a31b7-111">EXAMPLES</span></span>

### <span data-ttu-id="a31b7-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a31b7-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="a31b7-113">Yukarıdaki örnek, giriş parametresi olarak ad temelinde Azure 'dan myDMProject adlı Azure veritabanı geçiş hizmeti projesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="a31b7-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="a31b7-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a31b7-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="a31b7-115">Yukarıdaki örnek, Azure veritabanı geçiş hizmeti projesini, PSProject nesnesini giriş parametresi olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a31b7-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="a31b7-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a31b7-116">PARAMETERS</span></span>

### <span data-ttu-id="a31b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31b7-117">-DefaultProfile</span></span>
<span data-ttu-id="a31b7-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a31b7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a31b7-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="a31b7-119">-DeleteRunningTask</span></span>
<span data-ttu-id="a31b7-120">Çalışan görevleri silme</span><span class="sxs-lookup"><span data-stu-id="a31b7-120">Delete any running task</span></span>

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

### <span data-ttu-id="a31b7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a31b7-121">-Force</span></span>
<span data-ttu-id="a31b7-122">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="a31b7-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a31b7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a31b7-123">-InputObject</span></span>
<span data-ttu-id="a31b7-124">PSProject nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a31b7-124">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a31b7-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="a31b7-125">-Name</span></span>
<span data-ttu-id="a31b7-126">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="a31b7-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a31b7-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a31b7-127">-PassThru</span></span>
<span data-ttu-id="a31b7-128">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="a31b7-128">Returns an true/false.</span></span>
<span data-ttu-id="a31b7-129">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a31b7-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a31b7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a31b7-130">-ResourceGroupName</span></span>
<span data-ttu-id="a31b7-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a31b7-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a31b7-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a31b7-132">-ResourceId</span></span>
<span data-ttu-id="a31b7-133">Proje kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a31b7-133">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31b7-134">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="a31b7-134">-ServiceName</span></span>
<span data-ttu-id="a31b7-135">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="a31b7-135">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a31b7-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="a31b7-136">-Confirm</span></span>
<span data-ttu-id="a31b7-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a31b7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a31b7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a31b7-138">-WhatIf</span></span>
<span data-ttu-id="a31b7-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a31b7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a31b7-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a31b7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a31b7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31b7-141">CommonParameters</span></span>
<span data-ttu-id="a31b7-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a31b7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31b7-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a31b7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31b7-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a31b7-144">INPUTS</span></span>

### <span data-ttu-id="a31b7-145">Microsoft. Azure. Commands. DataMigration. modeller. PSProject</span><span class="sxs-lookup"><span data-stu-id="a31b7-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="a31b7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a31b7-146">System.String</span></span>

## <span data-ttu-id="a31b7-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a31b7-147">OUTPUTS</span></span>

### <span data-ttu-id="a31b7-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a31b7-148">System.Boolean</span></span>

## <span data-ttu-id="a31b7-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a31b7-149">NOTES</span></span>

## <span data-ttu-id="a31b7-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a31b7-150">RELATED LINKS</span></span>