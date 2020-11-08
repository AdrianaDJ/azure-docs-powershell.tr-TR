---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 287e4db59ae19efec604da9b63958b5ea74b747f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267774"
---
# <span data-ttu-id="5d397-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5d397-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="5d397-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d397-102">SYNOPSIS</span></span>
<span data-ttu-id="5d397-103">Azure veritabanı geçiş hizmeti 'nin bir örneğiyle ilişkili özellikleri getirir.</span><span class="sxs-lookup"><span data-stu-id="5d397-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="5d397-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d397-104">SYNTAX</span></span>

### <span data-ttu-id="5d397-105">ResourceGroupSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5d397-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d397-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5d397-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d397-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="5d397-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d397-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d397-108">DESCRIPTION</span></span>
<span data-ttu-id="5d397-109">Get-AzDataMigrationService cmdlet 'i, hizmet adına ve Azure Kaynak grubu adına bağlı olarak Azure veritabanı geçiş hizmeti 'nin bir örneğiyle ilişkili özellikleri giriş parametreleri olarak alır.</span><span class="sxs-lookup"><span data-stu-id="5d397-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="5d397-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d397-110">EXAMPLES</span></span>

### <span data-ttu-id="5d397-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5d397-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="5d397-112">Yukarıdaki örnek testService adındaki Azure veritabanı geçiş hizmeti örneğinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5d397-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="5d397-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5d397-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="5d397-114">Yukarıdaki örnek, testResourceGroup adındaki kaynak grubunda Azure veritabanı geçiş Hizmetleri 'ni alır.</span><span class="sxs-lookup"><span data-stu-id="5d397-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="5d397-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d397-115">PARAMETERS</span></span>

### <span data-ttu-id="5d397-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d397-116">-DefaultProfile</span></span>
<span data-ttu-id="5d397-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5d397-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d397-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="5d397-118">-Name</span></span>
<span data-ttu-id="5d397-119">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="5d397-119">Name of Database Migration Service.</span></span>

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

### <span data-ttu-id="5d397-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d397-120">-ResourceGroupName</span></span>
<span data-ttu-id="5d397-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5d397-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d397-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5d397-122">-ResourceId</span></span>
<span data-ttu-id="5d397-123">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="5d397-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="5d397-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d397-124">CommonParameters</span></span>
<span data-ttu-id="5d397-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d397-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d397-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d397-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d397-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d397-127">INPUTS</span></span>

### <span data-ttu-id="5d397-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5d397-128">System.String</span></span>

## <span data-ttu-id="5d397-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d397-129">OUTPUTS</span></span>

### <span data-ttu-id="5d397-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5d397-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="5d397-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d397-131">NOTES</span></span>

## <span data-ttu-id="5d397-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d397-132">RELATED LINKS</span></span>
