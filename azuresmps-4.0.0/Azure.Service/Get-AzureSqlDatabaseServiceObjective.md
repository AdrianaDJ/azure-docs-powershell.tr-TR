---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105568"
---
# <span data-ttu-id="073c5-101">Get-AzureSqlDatabaseServiceObjective</span><span class="sxs-lookup"><span data-stu-id="073c5-101">Get-AzureSqlDatabaseServiceObjective</span></span>

## <span data-ttu-id="073c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="073c5-102">SYNOPSIS</span></span>
<span data-ttu-id="073c5-103">Bir Azure SQL veritabanı sunucusu için hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="073c5-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="073c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="073c5-104">SYNTAX</span></span>

### <span data-ttu-id="073c5-105">ByConnectionContext (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="073c5-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="073c5-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="073c5-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="073c5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="073c5-107">DESCRIPTION</span></span>
<span data-ttu-id="073c5-108">**Get-azures, Databaseserviceamacın** cmdlet 'ı BIR Azure SQL veritabanı sunucusu için hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="073c5-108">The **Get-AzureSqlDatabaseServiceObjective** cmdlet gets service objectives for an Azure SQL Database server.</span></span>
<span data-ttu-id="073c5-109">Hizmet hedeflerine performans düzeyleri denir.</span><span class="sxs-lookup"><span data-stu-id="073c5-109">Service objectives are referred to as performance levels.</span></span>
<span data-ttu-id="073c5-110">Hizmet hedefi belirtmezseniz, bu cmdlet belirtilen sunucunun geçerli tüm hizmet amaçlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="073c5-110">If you do not specify a service objective, this cmdlet returns all valid service objectives for the specified server.</span></span>

<span data-ttu-id="073c5-111">Bu cmdlet, temel, standart ve Premium hizmet katmanlarına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="073c5-111">This cmdlet applies to Basic, Standard, and Premium service tiers.</span></span>

## <span data-ttu-id="073c5-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="073c5-112">EXAMPLES</span></span>

### <span data-ttu-id="073c5-113">Örnek 1: bağlantı bağlamı kullanarak tüm hizmet amaçlarını alma</span><span class="sxs-lookup"><span data-stu-id="073c5-113">Example 1: Get all the service objectives by using a connection context</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

<span data-ttu-id="073c5-114">Bu komut, bağlantı $Context bağlamının belirttiği sunucunun tüm hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="073c5-114">This command gets all the service objectives for the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="073c5-115">Örnek 2: sunucu adı kullanarak tüm hizmet amaçlarını alma</span><span class="sxs-lookup"><span data-stu-id="073c5-115">Example 2: Get all the service objectives by using a server name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

<span data-ttu-id="073c5-116">Bu komut, server01 adındaki sunucunun tüm hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="073c5-116">This command gets all the service objectives for the server named Server01.</span></span>

## <span data-ttu-id="073c5-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="073c5-117">PARAMETERS</span></span>

### <span data-ttu-id="073c5-118">-Context</span><span class="sxs-lookup"><span data-stu-id="073c5-118">-Context</span></span>
<span data-ttu-id="073c5-119">Sunucunun bağlantı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="073c5-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="073c5-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="073c5-120">-Profile</span></span>
<span data-ttu-id="073c5-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="073c5-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="073c5-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="073c5-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073c5-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="073c5-123">-ServerName</span></span>
<span data-ttu-id="073c5-124">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="073c5-124">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="073c5-125">-Serviceamacın</span><span class="sxs-lookup"><span data-stu-id="073c5-125">-ServiceObjective</span></span>
<span data-ttu-id="073c5-126">Bu cmdlet 'in aldığı hizmet hedefini temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="073c5-126">Specifies an object that represents the service objective that this cmdlet gets.</span></span>
<span data-ttu-id="073c5-127">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="073c5-127">Valid values are:</span></span> 

- <span data-ttu-id="073c5-128">Temel: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="073c5-128">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="073c5-129">Standart (S0): f1173c43-91bd-4AAA-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="073c5-129">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="073c5-130">Standart (S1): 1b1ebd4d-vseç903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="073c5-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="073c5-131">Standart (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="073c5-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="073c5-132">\* Standart (S3): 789681b8-CA10-4EB0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="073c5-132">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="073c5-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="073c5-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="073c5-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="073c5-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="073c5-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="073c5-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="073c5-136">Premium (P3): a7c4c615-cfb1-464B-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="073c5-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="073c5-137">\* Standart (S3) en son SQL veritabanı güncelleştirme V12 (Önizleme) parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="073c5-137">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="073c5-138">Daha fazla bilgi için, Azure kitaplığındaki [Azure SQL Veritabanı V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) () Ile sunulan yenilikleri görün `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` .</span><span class="sxs-lookup"><span data-stu-id="073c5-138">For more information, see [What's New in the Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) (`https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/`) in the Azure library.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="073c5-139">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="073c5-139">-ServiceObjectiveName</span></span>
<span data-ttu-id="073c5-140">Alınacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="073c5-140">Specifies the name of a service objective to get.</span></span>
<span data-ttu-id="073c5-141">Geçerli değerler: Basic, S0, S1, S2, S3, P1, P2 ve P3.</span><span class="sxs-lookup"><span data-stu-id="073c5-141">Valid values are: Basic, S0, S1, S2, S3, P1, P2, and P3.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073c5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="073c5-142">CommonParameters</span></span>
<span data-ttu-id="073c5-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="073c5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="073c5-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="073c5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="073c5-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="073c5-145">INPUTS</span></span>

### <span data-ttu-id="073c5-146">Microsoft. Windowsazde. Commands. SqlDatabase. Services. Server. Serviceamacın</span><span class="sxs-lookup"><span data-stu-id="073c5-146">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective</span></span>

## <span data-ttu-id="073c5-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="073c5-147">OUTPUTS</span></span>

### <span data-ttu-id="073c5-148">'A\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span><span class="sxs-lookup"><span data-stu-id="073c5-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span></span>

## <span data-ttu-id="073c5-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="073c5-149">NOTES</span></span>

## <span data-ttu-id="073c5-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="073c5-150">RELATED LINKS</span></span>

[<span data-ttu-id="073c5-151">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="073c5-151">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="073c5-152">Hizmet düzeyi amacını alma</span><span class="sxs-lookup"><span data-stu-id="073c5-152">Get Service Level Objective</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[<span data-ttu-id="073c5-153">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="073c5-153">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="073c5-154">New-Azuressqldatabaseservercontext</span><span class="sxs-lookup"><span data-stu-id="073c5-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


