---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 00a0e0a688f49615cadff3990071cd49d1356443
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761041"
---
# <span data-ttu-id="1b6e2-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="1b6e2-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="1b6e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b6e2-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6e2-103">Azure veritabanı geçiş projesi özelliklerini getirir.</span><span class="sxs-lookup"><span data-stu-id="1b6e2-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="1b6e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b6e2-104">SYNTAX</span></span>

### <span data-ttu-id="1b6e2-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1b6e2-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b6e2-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="1b6e2-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b6e2-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="1b6e2-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b6e2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b6e2-108">DESCRIPTION</span></span>
<span data-ttu-id="1b6e2-109">Get-AzDataMigrationProject cmdlet 'i, Azure veritabanı geçiş projesi özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="1b6e2-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="1b6e2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b6e2-110">EXAMPLES</span></span>

### <span data-ttu-id="1b6e2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b6e2-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="1b6e2-112">Yukarıdaki örnek testresourcegroup adındaki ve testhizmeti adlı hizmet 'in altındaki test</span><span class="sxs-lookup"><span data-stu-id="1b6e2-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="1b6e2-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1b6e2-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="1b6e2-114">Yukarıdaki örnek, gelen PSProject nesne giriş parametresine dayalı olarak Azure veritabanı geçiş projesini alır.</span><span class="sxs-lookup"><span data-stu-id="1b6e2-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="1b6e2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b6e2-115">PARAMETERS</span></span>

### <span data-ttu-id="1b6e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6e2-116">-DefaultProfile</span></span>
<span data-ttu-id="1b6e2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b6e2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b6e2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b6e2-118">-InputObject</span></span>
<span data-ttu-id="1b6e2-119">PSDataMigrationService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1b6e2-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="1b6e2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b6e2-120">-Name</span></span>
<span data-ttu-id="1b6e2-121">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="1b6e2-121">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b6e2-122">-ResourceGroupName</span></span>
<span data-ttu-id="1b6e2-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1b6e2-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="1b6e2-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1b6e2-124">-ResourceId</span></span>
<span data-ttu-id="1b6e2-125">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1b6e2-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="1b6e2-126">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="1b6e2-126">-ServiceName</span></span>
<span data-ttu-id="1b6e2-127">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="1b6e2-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="1b6e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6e2-128">CommonParameters</span></span>
<span data-ttu-id="1b6e2-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b6e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6e2-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b6e2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6e2-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b6e2-131">INPUTS</span></span>

### <span data-ttu-id="1b6e2-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="1b6e2-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="1b6e2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1b6e2-133">System.String</span></span>

## <span data-ttu-id="1b6e2-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b6e2-134">OUTPUTS</span></span>

### <span data-ttu-id="1b6e2-135">Microsoft. Azure. Commands. DataMigration. modeller. PSProject</span><span class="sxs-lookup"><span data-stu-id="1b6e2-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="1b6e2-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b6e2-136">NOTES</span></span>

## <span data-ttu-id="1b6e2-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b6e2-137">RELATED LINKS</span></span>