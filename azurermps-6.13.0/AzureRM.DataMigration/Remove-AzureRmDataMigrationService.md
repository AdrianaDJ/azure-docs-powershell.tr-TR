---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: 677e89dd0def314744e507c6e61c745f39a081bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593672"
---
# <span data-ttu-id="1a1bc-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="1a1bc-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="1a1bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a1bc-102">SYNOPSIS</span></span>
<span data-ttu-id="1a1bc-103">Azure veritabanı geçiş hizmeti 'nin bir örneğini Azure 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a1bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a1bc-104">SYNTAX</span></span>

### <span data-ttu-id="1a1bc-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1a1bc-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a1bc-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="1a1bc-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a1bc-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="1a1bc-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a1bc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a1bc-108">DESCRIPTION</span></span>
<span data-ttu-id="1a1bc-109">Remove-AzureRmDataMigrationService cmdlet 'i Azure veritabanı geçiş hizmeti 'nin Azure 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="1a1bc-110">DeleteRunningTask parametresi sağlanırken, kaldırılmakta olan hizmetle ilişkili tüm Azure veritabanı geçiş hizmeti görevleri kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="1a1bc-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a1bc-111">EXAMPLES</span></span>

### <span data-ttu-id="1a1bc-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1a1bc-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="1a1bc-113">Yukarıdaki örnek, MyResourceGroup adlı bir Azure Kaynak grubunda bulunan TestService adındaki bir Azure veritabanı geçiş hizmeti örneğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="1a1bc-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a1bc-114">PARAMETERS</span></span>

### <span data-ttu-id="1a1bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a1bc-115">-DefaultProfile</span></span>
<span data-ttu-id="1a1bc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a1bc-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="1a1bc-117">-DeleteRunningTask</span></span>
<span data-ttu-id="1a1bc-118">Çalışan görevleri silme</span><span class="sxs-lookup"><span data-stu-id="1a1bc-118">Delete any running task</span></span>

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

### <span data-ttu-id="1a1bc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1a1bc-119">-Force</span></span>
<span data-ttu-id="1a1bc-120">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="1a1bc-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1a1bc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a1bc-121">-InputObject</span></span>
<span data-ttu-id="1a1bc-122">PSDataMigrationService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="1a1bc-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a1bc-123">-Name</span></span>
<span data-ttu-id="1a1bc-124">Veritabanı geçiş hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="1a1bc-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1a1bc-125">-PassThru</span></span>
<span data-ttu-id="1a1bc-126">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-126">Returns an true/false.</span></span>
<span data-ttu-id="1a1bc-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1a1bc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a1bc-128">-ResourceGroupName</span></span>
<span data-ttu-id="1a1bc-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="1a1bc-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1a1bc-130">-ResourceId</span></span>
<span data-ttu-id="1a1bc-131">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="1a1bc-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="1a1bc-132">-Confirm</span></span>
<span data-ttu-id="1a1bc-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a1bc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a1bc-134">-WhatIf</span></span>
<span data-ttu-id="1a1bc-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a1bc-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a1bc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a1bc-137">CommonParameters</span></span>
<span data-ttu-id="1a1bc-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a1bc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a1bc-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a1bc-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a1bc-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a1bc-140">INPUTS</span></span>

### <span data-ttu-id="1a1bc-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="1a1bc-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="1a1bc-142">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1a1bc-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1a1bc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1a1bc-143">System.String</span></span>

## <span data-ttu-id="1a1bc-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a1bc-144">OUTPUTS</span></span>

### <span data-ttu-id="1a1bc-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a1bc-145">System.Boolean</span></span>

## <span data-ttu-id="1a1bc-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a1bc-146">NOTES</span></span>

## <span data-ttu-id="1a1bc-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a1bc-147">RELATED LINKS</span></span>
