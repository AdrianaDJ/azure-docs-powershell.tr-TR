---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: 06899e35e9119025aa13a310a3d6200c30b223df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591974"
---
# <span data-ttu-id="9b38a-101">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9b38a-101">Get-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="9b38a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b38a-102">SYNOPSIS</span></span>
<span data-ttu-id="9b38a-103">Azure veritabanı geçiş hizmeti 'nin bir örneğiyle ilişkili özellikleri getirir.</span><span class="sxs-lookup"><span data-stu-id="9b38a-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b38a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b38a-104">SYNTAX</span></span>

### <span data-ttu-id="9b38a-105">ResourceGroupSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9b38a-105">ResourceGroupSet (Default)</span></span>
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b38a-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9b38a-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b38a-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="9b38a-107">ServiceNameGroupSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b38a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b38a-108">DESCRIPTION</span></span>
<span data-ttu-id="9b38a-109">Get-AzureRmDataMigrationService cmdlet 'i, hizmet adına ve Azure Kaynak grubu adına bağlı olarak Azure veritabanı geçiş hizmeti 'nin bir örneğiyle ilişkili özellikleri giriş parametreleri olarak alır.</span><span class="sxs-lookup"><span data-stu-id="9b38a-109">The Get-AzureRmDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="9b38a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b38a-110">EXAMPLES</span></span>

### <span data-ttu-id="9b38a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9b38a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="9b38a-112">Yukarıdaki örnek testService adındaki Azure veritabanı geçiş hizmeti örneğinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="9b38a-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="9b38a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9b38a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="9b38a-114">Yukarıdaki örnek, testResourceGroup adındaki kaynak grubunda Azure veritabanı geçiş Hizmetleri 'ni alır.</span><span class="sxs-lookup"><span data-stu-id="9b38a-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="9b38a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b38a-115">PARAMETERS</span></span>

### <span data-ttu-id="9b38a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b38a-116">-DefaultProfile</span></span>
<span data-ttu-id="9b38a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b38a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b38a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="9b38a-118">-Name</span></span>
<span data-ttu-id="9b38a-119">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="9b38a-119">Name of Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b38a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b38a-120">-ResourceGroupName</span></span>
<span data-ttu-id="9b38a-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9b38a-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b38a-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9b38a-122">-ResourceId</span></span>
<span data-ttu-id="9b38a-123">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9b38a-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="9b38a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b38a-124">CommonParameters</span></span>
<span data-ttu-id="9b38a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b38a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b38a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b38a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b38a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b38a-127">INPUTS</span></span>

### <span data-ttu-id="9b38a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9b38a-128">System.String</span></span>

## <span data-ttu-id="9b38a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b38a-129">OUTPUTS</span></span>

### <span data-ttu-id="9b38a-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9b38a-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="9b38a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b38a-131">NOTES</span></span>

## <span data-ttu-id="9b38a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b38a-132">RELATED LINKS</span></span>