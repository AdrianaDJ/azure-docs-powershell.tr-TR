---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: ea6406d83004d9a7d21a2f47aba0c39a10caf59a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593505"
---
# <span data-ttu-id="2b26a-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="2b26a-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="2b26a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b26a-102">SYNOPSIS</span></span>
<span data-ttu-id="2b26a-103">Azure veritabanı geçiş projesi özelliklerini getirir.</span><span class="sxs-lookup"><span data-stu-id="2b26a-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b26a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b26a-104">SYNTAX</span></span>

### <span data-ttu-id="2b26a-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2b26a-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2b26a-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="2b26a-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2b26a-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2b26a-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="2b26a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b26a-108">DESCRIPTION</span></span>
<span data-ttu-id="2b26a-109">Get-AzureRmDataMigrationProject cmdlet 'i, Azure veritabanı geçiş projesi özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="2b26a-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="2b26a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b26a-110">EXAMPLES</span></span>

### <span data-ttu-id="2b26a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2b26a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="2b26a-112">Yukarıdaki örnek testresourcegroup adındaki ve testhizmeti adlı hizmet 'in altındaki test</span><span class="sxs-lookup"><span data-stu-id="2b26a-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="2b26a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2b26a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="2b26a-114">Yukarıdaki örnek, gelen PSProject nesne giriş parametresine dayalı olarak Azure veritabanı geçiş projesini alır.</span><span class="sxs-lookup"><span data-stu-id="2b26a-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 


## <span data-ttu-id="2b26a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b26a-115">PARAMETERS</span></span>

### <span data-ttu-id="2b26a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b26a-116">-DefaultProfile</span></span>
<span data-ttu-id="2b26a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b26a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b26a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b26a-118">-InputObject</span></span>
<span data-ttu-id="2b26a-119">PSDataMigrationService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2b26a-119">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b26a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b26a-120">-Name</span></span>
<span data-ttu-id="2b26a-121">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="2b26a-121">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b26a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b26a-122">-ResourceGroupName</span></span>
<span data-ttu-id="2b26a-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2b26a-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b26a-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2b26a-124">-ResourceId</span></span>
<span data-ttu-id="2b26a-125">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="2b26a-125">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b26a-126">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="2b26a-126">-ServiceName</span></span>
<span data-ttu-id="2b26a-127">Veri geçişi hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="2b26a-127">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="2b26a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b26a-128">INPUTS</span></span>

### <span data-ttu-id="2b26a-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2b26a-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="2b26a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2b26a-130">System.String</span></span>


## <span data-ttu-id="2b26a-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b26a-131">OUTPUTS</span></span>

### <span data-ttu-id="2b26a-132">System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. DataMigration. modeller. PSProject, Microsoft. Azure. Commands. DataMigration, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2b26a-132">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProject, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="2b26a-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b26a-133">NOTES</span></span>

## <span data-ttu-id="2b26a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b26a-134">RELATED LINKS</span></span>

