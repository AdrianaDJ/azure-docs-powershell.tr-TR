---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: b3978bcc0e3b883d95c5161ca1b24f9cd6c6c1f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752239"
---
# <span data-ttu-id="95ce5-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="95ce5-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="95ce5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="95ce5-103">Azure veritabanı geçiş hizmeti 'nin yeni bir örneğini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="95ce5-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="95ce5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95ce5-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95ce5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="95ce5-105">DESCRIPTION</span></span>
<span data-ttu-id="95ce5-106">New-AzDataMigrationService cmdlet 'i Azure veritabanı geçiş hizmeti 'nin yeni bir örneğini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="95ce5-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="95ce5-107">Bu cmdlet, var olan Azure Resource grubunun adını, Azure veritabanı geçiş hizmeti 'nin yeni örneğinin oluşturulması için benzersiz adı, örneğin sağlandıkları bölgeyi, DMS çalışan SKU 'nun adını ve hizmetin bulunacağı Azure sanal alt ağının adını alır.</span><span class="sxs-lookup"><span data-stu-id="95ce5-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="95ce5-108">Abonelik adında parametre yoksa, kullanıcının Azure oturum açma oturumunun varsayılan aboneliğini belirtmesi veya Get-AzSubscription-SubscriptionName "MySubscription" | Başka bir abonelik seçmek için Select-AzSubscription.</span><span class="sxs-lookup"><span data-stu-id="95ce5-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="95ce5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95ce5-109">EXAMPLES</span></span>

### <span data-ttu-id="95ce5-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="95ce5-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="95ce5-111">Yukarıdaki örnekte, Merkezi ABD bölgesindeki TestService adlı Azure veritabanı geçiş hizmeti örneğinin nasıl oluşturulacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="95ce5-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="95ce5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95ce5-112">PARAMETERS</span></span>

### <span data-ttu-id="95ce5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ce5-113">-DefaultProfile</span></span>
<span data-ttu-id="95ce5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95ce5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95ce5-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="95ce5-115">-Location</span></span>
<span data-ttu-id="95ce5-116">Oluşturulacak Azure veritabanı geçiş hizmeti örneğinin konumu, bir Azure bölgesine karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="95ce5-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="95ce5-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="95ce5-117">-Name</span></span>
<span data-ttu-id="95ce5-118">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="95ce5-118">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="95ce5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ce5-119">-ResourceGroupName</span></span>
<span data-ttu-id="95ce5-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="95ce5-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="95ce5-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="95ce5-121">-Sku</span></span>
<span data-ttu-id="95ce5-122">Azure veritabanı geçiş hizmeti örneğinin SKU 'su.</span><span class="sxs-lookup"><span data-stu-id="95ce5-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="95ce5-123">Şu anda olası değerler Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="95ce5-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="95ce5-124">-Virtualsubnetıd</span><span class="sxs-lookup"><span data-stu-id="95ce5-124">-VirtualSubnetId</span></span>
<span data-ttu-id="95ce5-125">Azure veritabanı geçiş hizmeti örneğinde kullanılacak sanal ağın altındaki alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="95ce5-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="95ce5-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="95ce5-126">-Confirm</span></span>
<span data-ttu-id="95ce5-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="95ce5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95ce5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95ce5-128">-WhatIf</span></span>
<span data-ttu-id="95ce5-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="95ce5-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95ce5-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="95ce5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95ce5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ce5-131">CommonParameters</span></span>
<span data-ttu-id="95ce5-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95ce5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ce5-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95ce5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ce5-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95ce5-134">INPUTS</span></span>

### <span data-ttu-id="95ce5-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="95ce5-135">None</span></span>

## <span data-ttu-id="95ce5-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95ce5-136">OUTPUTS</span></span>

### <span data-ttu-id="95ce5-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="95ce5-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="95ce5-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95ce5-138">NOTES</span></span>

## <span data-ttu-id="95ce5-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95ce5-139">RELATED LINKS</span></span>
