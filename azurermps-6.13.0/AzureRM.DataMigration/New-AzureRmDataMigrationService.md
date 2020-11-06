---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: cc2f708294be05b16b0c5be94fb9da260b479799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591969"
---
# <span data-ttu-id="88425-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="88425-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="88425-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88425-102">SYNOPSIS</span></span>
<span data-ttu-id="88425-103">Azure veritabanı geçiş hizmeti 'nin yeni bir örneğini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="88425-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88425-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88425-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88425-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="88425-105">DESCRIPTION</span></span>
<span data-ttu-id="88425-106">New-AzureRmDataMigrationService cmdlet 'i Azure veritabanı geçiş hizmeti 'nin yeni bir örneğini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="88425-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="88425-107">Bu cmdlet, var olan Azure Resource grubunun adını, Azure veritabanı geçiş hizmeti 'nin yeni örneğinin oluşturulması için benzersiz adı, örneğin sağlandıkları bölgeyi, DMS çalışan SKU 'nun adını ve hizmetin bulunacağı Azure sanal alt ağının adını alır.</span><span class="sxs-lookup"><span data-stu-id="88425-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="88425-108">Abonelik adında parametre yoksa, kullanıcının Azure oturum açma oturumunun varsayılan aboneliğini belirtmesi veya Get-AzureRmSubscription-SubscriptionName "MySubscription" | Başka bir abonelik seçmek için Select-AzureRmSubscription.</span><span class="sxs-lookup"><span data-stu-id="88425-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription -SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="88425-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88425-109">EXAMPLES</span></span>

### <span data-ttu-id="88425-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="88425-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="88425-111">Yukarıdaki örnekte, Merkezi ABD bölgesindeki TestService adlı Azure veritabanı geçiş hizmeti örneğinin nasıl oluşturulacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="88425-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="88425-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88425-112">PARAMETERS</span></span>

### <span data-ttu-id="88425-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88425-113">-DefaultProfile</span></span>
<span data-ttu-id="88425-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88425-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88425-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="88425-115">-Location</span></span>
<span data-ttu-id="88425-116">Oluşturulacak Azure veritabanı geçiş hizmeti örneğinin konumu, bir Azure bölgesine karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="88425-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88425-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="88425-117">-Name</span></span>
<span data-ttu-id="88425-118">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="88425-118">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88425-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88425-119">-ResourceGroupName</span></span>
<span data-ttu-id="88425-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="88425-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88425-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="88425-121">-Sku</span></span>
<span data-ttu-id="88425-122">Azure veritabanı geçiş hizmeti örneğinin SKU 'su.</span><span class="sxs-lookup"><span data-stu-id="88425-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="88425-123">Şu anda olası değerler Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="88425-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88425-124">-Virtualsubnetıd</span><span class="sxs-lookup"><span data-stu-id="88425-124">-VirtualSubnetId</span></span>
<span data-ttu-id="88425-125">Azure veritabanı geçiş hizmeti örneğinde kullanılacak sanal ağın altındaki alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="88425-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88425-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="88425-126">-Confirm</span></span>
<span data-ttu-id="88425-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="88425-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88425-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88425-128">-WhatIf</span></span>
<span data-ttu-id="88425-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="88425-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88425-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="88425-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88425-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88425-131">CommonParameters</span></span>
<span data-ttu-id="88425-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88425-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88425-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88425-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88425-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88425-134">INPUTS</span></span>

### <span data-ttu-id="88425-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="88425-135">None</span></span>

## <span data-ttu-id="88425-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88425-136">OUTPUTS</span></span>

### <span data-ttu-id="88425-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="88425-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="88425-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88425-138">NOTES</span></span>

## <span data-ttu-id="88425-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88425-139">RELATED LINKS</span></span>
