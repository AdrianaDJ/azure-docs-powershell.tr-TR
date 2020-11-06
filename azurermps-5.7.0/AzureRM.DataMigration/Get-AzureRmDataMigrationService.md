---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: cac57ff34d925d553c25d97facd81dba017a25c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591682"
---
# <span data-ttu-id="9f5ac-101">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9f5ac-101">Get-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="9f5ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f5ac-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5ac-103">Azure veritabanı geçiş hizmeti 'nin bir örneğiyle ilişkili özellikleri getirir.</span><span class="sxs-lookup"><span data-stu-id="9f5ac-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f5ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f5ac-104">SYNTAX</span></span>

### <span data-ttu-id="9f5ac-105">ResourceGroupSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9f5ac-105">ResourceGroupSet (Default)</span></span>
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="9f5ac-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9f5ac-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="9f5ac-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="9f5ac-107">ServiceNameGroupSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>]
```
## <span data-ttu-id="9f5ac-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f5ac-108">DESCRIPTION</span></span>
<span data-ttu-id="9f5ac-109">Get-AzureRmDataMigrationService cmdlet 'i, hizmet adına ve Azure Kaynak grubu adına bağlı olarak Azure veritabanı geçiş hizmeti 'nin bir örneğiyle ilişkili özellikleri giriş parametreleri olarak alır.</span><span class="sxs-lookup"><span data-stu-id="9f5ac-109">The Get-AzureRmDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="9f5ac-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f5ac-110">EXAMPLES</span></span>

### <span data-ttu-id="9f5ac-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9f5ac-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="9f5ac-112">Yukarıdaki örnek testService adındaki Azure veritabanı geçiş hizmeti örneğinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="9f5ac-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="9f5ac-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9f5ac-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup 
```

<span data-ttu-id="9f5ac-114">Yukarıdaki örnek, testResourceGroup adındaki kaynak grubunda Azure veritabanı geçiş Hizmetleri 'ni alır.</span><span class="sxs-lookup"><span data-stu-id="9f5ac-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="9f5ac-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f5ac-115">PARAMETERS</span></span>

### <span data-ttu-id="9f5ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5ac-116">-DefaultProfile</span></span>
<span data-ttu-id="9f5ac-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f5ac-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f5ac-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f5ac-118">-Name</span></span>
<span data-ttu-id="9f5ac-119">Veri geçişi hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="9f5ac-119">Name of Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f5ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="9f5ac-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9f5ac-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5ac-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9f5ac-122">-ResourceId</span></span>
<span data-ttu-id="9f5ac-123">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9f5ac-123">DataMigrationService Resource Id.</span></span>

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

## <span data-ttu-id="9f5ac-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f5ac-124">INPUTS</span></span>

### <span data-ttu-id="9f5ac-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9f5ac-125">System.String</span></span>


## <span data-ttu-id="9f5ac-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f5ac-126">OUTPUTS</span></span>

### <span data-ttu-id="9f5ac-127">System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft. Azure. Commands. DataMigration, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9f5ac-127">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="9f5ac-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f5ac-128">NOTES</span></span>

## <span data-ttu-id="9f5ac-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f5ac-129">RELATED LINKS</span></span>





