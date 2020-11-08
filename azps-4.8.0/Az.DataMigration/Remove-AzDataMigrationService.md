---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 2ba182833fc1d4c59d9164b6db5d68bcd3c499f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268299"
---
# <span data-ttu-id="ea1df-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ea1df-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="ea1df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea1df-102">SYNOPSIS</span></span>
<span data-ttu-id="ea1df-103">Azure veritabanı geçiş hizmeti 'nin bir örneğini Azure 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ea1df-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="ea1df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea1df-104">SYNTAX</span></span>

### <span data-ttu-id="ea1df-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ea1df-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea1df-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="ea1df-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea1df-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ea1df-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea1df-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea1df-108">DESCRIPTION</span></span>
<span data-ttu-id="ea1df-109">Remove-AzDataMigrationService cmdlet 'i Azure veritabanı geçiş hizmeti 'nin Azure 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ea1df-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="ea1df-110">DeleteRunningTask parametresi sağlanırken, kaldırılmakta olan hizmetle ilişkili tüm Azure veritabanı geçiş hizmeti görevleri kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="ea1df-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="ea1df-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea1df-111">EXAMPLES</span></span>

### <span data-ttu-id="ea1df-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ea1df-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="ea1df-113">Yukarıdaki örnek, MyResourceGroup adlı bir Azure Kaynak grubunda bulunan TestService adındaki bir Azure veritabanı geçiş hizmeti örneğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ea1df-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="ea1df-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea1df-114">PARAMETERS</span></span>

### <span data-ttu-id="ea1df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea1df-115">-DefaultProfile</span></span>
<span data-ttu-id="ea1df-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea1df-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea1df-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="ea1df-117">-DeleteRunningTask</span></span>
<span data-ttu-id="ea1df-118">Çalışan görevleri silme</span><span class="sxs-lookup"><span data-stu-id="ea1df-118">Delete any running task</span></span>

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

### <span data-ttu-id="ea1df-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ea1df-119">-Force</span></span>
<span data-ttu-id="ea1df-120">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="ea1df-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ea1df-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea1df-121">-InputObject</span></span>
<span data-ttu-id="ea1df-122">PSDataMigrationService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ea1df-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea1df-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea1df-123">-Name</span></span>
<span data-ttu-id="ea1df-124">Veritabanı geçiş hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="ea1df-124">The name of the Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea1df-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ea1df-125">-PassThru</span></span>
<span data-ttu-id="ea1df-126">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="ea1df-126">Returns an true/false.</span></span>
<span data-ttu-id="ea1df-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ea1df-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea1df-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea1df-128">-ResourceGroupName</span></span>
<span data-ttu-id="ea1df-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ea1df-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="ea1df-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ea1df-130">-ResourceId</span></span>
<span data-ttu-id="ea1df-131">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ea1df-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="ea1df-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea1df-132">-Confirm</span></span>
<span data-ttu-id="ea1df-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea1df-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea1df-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea1df-134">-WhatIf</span></span>
<span data-ttu-id="ea1df-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea1df-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea1df-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea1df-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea1df-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea1df-137">CommonParameters</span></span>
<span data-ttu-id="ea1df-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea1df-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea1df-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea1df-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea1df-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea1df-140">INPUTS</span></span>

### <span data-ttu-id="ea1df-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ea1df-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="ea1df-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ea1df-142">System.String</span></span>

## <span data-ttu-id="ea1df-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea1df-143">OUTPUTS</span></span>

### <span data-ttu-id="ea1df-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea1df-144">System.Boolean</span></span>

## <span data-ttu-id="ea1df-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea1df-145">NOTES</span></span>

## <span data-ttu-id="ea1df-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea1df-146">RELATED LINKS</span></span>
