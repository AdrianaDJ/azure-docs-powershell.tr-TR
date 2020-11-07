---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764457"
---
# <span data-ttu-id="340ca-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="340ca-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="340ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="340ca-102">SYNOPSIS</span></span>
<span data-ttu-id="340ca-103">Azure veritabanı geçiş hizmeti 'nin yeni bir örneğini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="340ca-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="340ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="340ca-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="340ca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="340ca-105">DESCRIPTION</span></span>
<span data-ttu-id="340ca-106">New-AzureRmDataMigrationService cmdlet 'i Azure veritabanı geçiş hizmeti 'nin yeni bir örneğini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="340ca-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="340ca-107">Bu cmdlet, var olan Azure Resource grubunun adını, Azure veritabanı geçiş hizmeti 'nin yeni örneğinin oluşturulması için benzersiz adı, örneğin sağlandıkları bölgeyi, DMS çalışan SKU 'nun adını ve hizmetin bulunacağı Azure sanal alt ağının adını alır.</span><span class="sxs-lookup"><span data-stu-id="340ca-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="340ca-108">Abonelik adında parametre yoksa, kullanıcının Azure oturumu açma oturumunun varsayılan aboneliğini belirtmesi veya Get-AzureRmSubscription-SubscriptionName "MySubscription" | Başka bir abonelik seçmek için Select-AzureRmSubscription.</span><span class="sxs-lookup"><span data-stu-id="340ca-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription –SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="340ca-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="340ca-109">EXAMPLES</span></span>

### <span data-ttu-id="340ca-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="340ca-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="340ca-111">Yukarıdaki örnekte, Merkezi ABD bölgesindeki TestService adlı Azure veritabanı geçiş hizmeti örneğinin nasıl oluşturulacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="340ca-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>


## <span data-ttu-id="340ca-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="340ca-112">PARAMETERS</span></span>

### <span data-ttu-id="340ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="340ca-113">-DefaultProfile</span></span>
<span data-ttu-id="340ca-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="340ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="340ca-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="340ca-115">-Location</span></span>
<span data-ttu-id="340ca-116">Oluşturulacak Azure veritabanı geçiş hizmeti örneğinin konumu, bir Azure bölgesine karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="340ca-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="340ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="340ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="340ca-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="340ca-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="340ca-119">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="340ca-119">-ServiceName</span></span>
<span data-ttu-id="340ca-120">Azure veritabanı geçiş hizmeti örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="340ca-120">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="340ca-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="340ca-121">-Sku</span></span>
<span data-ttu-id="340ca-122">Azure veritabanı geçiş hizmeti örneğinin SKU 'su.</span><span class="sxs-lookup"><span data-stu-id="340ca-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="340ca-123">Şu anda olası değerler Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="340ca-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="340ca-124">-Virtualsubnetıd</span><span class="sxs-lookup"><span data-stu-id="340ca-124">-VirtualSubnetId</span></span>
<span data-ttu-id="340ca-125">Azure veritabanı geçiş hizmeti örneğinde kullanılacak sanal ağın altındaki alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="340ca-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="340ca-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="340ca-126">OUTPUTS</span></span>

### <span data-ttu-id="340ca-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="340ca-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>


## <span data-ttu-id="340ca-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="340ca-128">NOTES</span></span>

## <span data-ttu-id="340ca-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="340ca-129">RELATED LINKS</span></span>

