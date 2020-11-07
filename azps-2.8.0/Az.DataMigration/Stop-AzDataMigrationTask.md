---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: 11ef118483d22451c908fcf7beefb7faae038622
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752224"
---
# <span data-ttu-id="fcae6-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="fcae6-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="fcae6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcae6-102">SYNOPSIS</span></span>
<span data-ttu-id="fcae6-103">Çalışmakta olan bir Azure veritabanı geçiş hizmeti görevini durdurur.</span><span class="sxs-lookup"><span data-stu-id="fcae6-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="fcae6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fcae6-104">SYNTAX</span></span>

### <span data-ttu-id="fcae6-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fcae6-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcae6-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="fcae6-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcae6-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="fcae6-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcae6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fcae6-108">DESCRIPTION</span></span>
<span data-ttu-id="fcae6-109">Stop-AzDataMigrationTask cmdlet, çalışma durumundaki veritabanı geçişi etkinliğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="fcae6-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="fcae6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fcae6-110">EXAMPLES</span></span>

### <span data-ttu-id="fcae6-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fcae6-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="fcae6-112">Yukarıdaki örnek, myDMSTask adlı Project Myvseçmsproject ve Azure veritabanı geçiş hizmeti</span><span class="sxs-lookup"><span data-stu-id="fcae6-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="fcae6-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fcae6-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="fcae6-114">Yukarıdaki örnek Azure veritabanı geçiş hizmeti görevini</span><span class="sxs-lookup"><span data-stu-id="fcae6-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="fcae6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fcae6-115">PARAMETERS</span></span>

### <span data-ttu-id="fcae6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcae6-116">-DefaultProfile</span></span>
<span data-ttu-id="fcae6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fcae6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcae6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcae6-118">-InputObject</span></span>
<span data-ttu-id="fcae6-119">PSProjectTask nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fcae6-119">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcae6-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="fcae6-120">-Name</span></span>
<span data-ttu-id="fcae6-121">Görevin adı.</span><span class="sxs-lookup"><span data-stu-id="fcae6-121">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcae6-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fcae6-122">-PassThru</span></span>
<span data-ttu-id="fcae6-123">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="fcae6-123">Returns an true/false.</span></span>
<span data-ttu-id="fcae6-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="fcae6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fcae6-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="fcae6-125">-ProjectName</span></span>
<span data-ttu-id="fcae6-126">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="fcae6-126">The name of the project.</span></span>

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

### <span data-ttu-id="fcae6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcae6-127">-ResourceGroupName</span></span>
<span data-ttu-id="fcae6-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fcae6-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="fcae6-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fcae6-129">-ResourceId</span></span>
<span data-ttu-id="fcae6-130">ProjectTask kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="fcae6-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="fcae6-131">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="fcae6-131">-ServiceName</span></span>
<span data-ttu-id="fcae6-132">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="fcae6-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="fcae6-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="fcae6-133">-Confirm</span></span>
<span data-ttu-id="fcae6-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fcae6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcae6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcae6-135">-WhatIf</span></span>
<span data-ttu-id="fcae6-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fcae6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcae6-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fcae6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcae6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcae6-138">CommonParameters</span></span>
<span data-ttu-id="fcae6-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fcae6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcae6-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcae6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcae6-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fcae6-141">INPUTS</span></span>

### <span data-ttu-id="fcae6-142">Microsoft. Azure. Commands. DataMigration. modeller. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="fcae6-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="fcae6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fcae6-143">System.String</span></span>

## <span data-ttu-id="fcae6-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fcae6-144">OUTPUTS</span></span>

### <span data-ttu-id="fcae6-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fcae6-145">System.Boolean</span></span>

## <span data-ttu-id="fcae6-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fcae6-146">NOTES</span></span>

## <span data-ttu-id="fcae6-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fcae6-147">RELATED LINKS</span></span>