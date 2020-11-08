---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280061"
---
# <span data-ttu-id="c84ed-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c84ed-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="c84ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c84ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c84ed-103">Kaydedilmiş kurtarma hizmetleri sağlayıcısının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c84ed-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="c84ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c84ed-104">SYNTAX</span></span>

### <span data-ttu-id="c84ed-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c84ed-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c84ed-106">Al</span><span class="sxs-lookup"><span data-stu-id="c84ed-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c84ed-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c84ed-107">DESCRIPTION</span></span>
<span data-ttu-id="c84ed-108">Kaydedilmiş kurtarma hizmetleri sağlayıcısının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c84ed-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="c84ed-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c84ed-109">EXAMPLES</span></span>

### <span data-ttu-id="c84ed-110">Örnek 1: kasaya tüm sağlayıcıları alma</span><span class="sxs-lookup"><span data-stu-id="c84ed-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="c84ed-111">Tümünü listeler.</span><span class="sxs-lookup"><span data-stu-id="c84ed-111">List all.</span></span>

## <span data-ttu-id="c84ed-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c84ed-112">PARAMETERS</span></span>

### <span data-ttu-id="c84ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c84ed-113">-DefaultProfile</span></span>
<span data-ttu-id="c84ed-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c84ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c84ed-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="c84ed-115">-FabricName</span></span>
<span data-ttu-id="c84ed-116">Doku adı.</span><span class="sxs-lookup"><span data-stu-id="c84ed-116">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c84ed-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="c84ed-117">-ProviderName</span></span>
<span data-ttu-id="c84ed-118">Kurtarma Hizmetleri sağlayıcı adı</span><span class="sxs-lookup"><span data-stu-id="c84ed-118">Recovery services provider name</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c84ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c84ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="c84ed-120">Kurtarma Hizmetleri kasasındaki kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c84ed-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="c84ed-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c84ed-121">-ResourceName</span></span>
<span data-ttu-id="c84ed-122">Kurtarma Hizmetleri kasasındaki adı.</span><span class="sxs-lookup"><span data-stu-id="c84ed-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="c84ed-123">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c84ed-123">-SubscriptionId</span></span>
<span data-ttu-id="c84ed-124">Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="c84ed-124">The subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c84ed-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c84ed-125">CommonParameters</span></span>
<span data-ttu-id="c84ed-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c84ed-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c84ed-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c84ed-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c84ed-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c84ed-128">INPUTS</span></span>

## <span data-ttu-id="c84ed-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c84ed-129">OUTPUTS</span></span>

### <span data-ttu-id="c84ed-130">Microsoft. Azure. PowerShell. cmdlet. Api20180110.</span><span class="sxs-lookup"><span data-stu-id="c84ed-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="c84ed-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c84ed-131">NOTES</span></span>

<span data-ttu-id="c84ed-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c84ed-132">ALIASES</span></span>

## <span data-ttu-id="c84ed-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c84ed-133">RELATED LINKS</span></span>

