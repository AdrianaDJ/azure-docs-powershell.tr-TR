---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106559"
---
# <span data-ttu-id="6dae1-101">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="6dae1-101">Get-AzureSqlRecoverableDatabase</span></span>

## <span data-ttu-id="6dae1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dae1-102">SYNOPSIS</span></span>
<span data-ttu-id="6dae1-103">Belirtilen sunucudan kurtarılabilir veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6dae1-103">Gets recoverable databases from a specified server.</span></span>

## <span data-ttu-id="6dae1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6dae1-104">SYNTAX</span></span>

### <span data-ttu-id="6dae1-105">AllDatabasesOnGivenServer (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6dae1-105">AllDatabasesOnGivenServer (Default)</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6dae1-106">Givendatabaseon sunucu</span><span class="sxs-lookup"><span data-stu-id="6dae1-106">GivenDatabaseOnGivenServer</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="6dae1-107">Givendatabasenesnesi</span><span class="sxs-lookup"><span data-stu-id="6dae1-107">GivenDatabaseObject</span></span>
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6dae1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6dae1-108">DESCRIPTION</span></span>
<span data-ttu-id="6dae1-109">**Get-Azuressqlrecoverabledatabase** cmdlet 'i belirtilen sunucudan kurtarılabilir veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6dae1-109">The **Get-AzureSqlRecoverableDatabase** cmdlet gets recoverable databases from a specified server.</span></span>
<span data-ttu-id="6dae1-110">Bu cmdlet, belirli bir kurtarılabilir veritabanını veya sunucudaki tüm kurtarılabilir veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6dae1-110">This cmdlet gets a specific recoverable database or all recoverable databases on a server.</span></span>

## <span data-ttu-id="6dae1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6dae1-111">EXAMPLES</span></span>

### <span data-ttu-id="6dae1-112">Örnek 1: tüm kurtarılabilir veritabanları</span><span class="sxs-lookup"><span data-stu-id="6dae1-112">Example 1: Get all recoverable databases</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

<span data-ttu-id="6dae1-113">Bu komut, server01 adlı sunucudaki tüm kurtarılabilir veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6dae1-113">This command gets all recoverable databases on the server named Server01.</span></span>

### <span data-ttu-id="6dae1-114">Örnek 2: kurtarılabilir bir veritabanı alma</span><span class="sxs-lookup"><span data-stu-id="6dae1-114">Example 2: Get a specific recoverable database</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

<span data-ttu-id="6dae1-115">Bu komut, server01 adındaki sunucuda Database17 adlı veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="6dae1-115">This command gets retrieves the database named Database17 on the server named Server01.</span></span>

## <span data-ttu-id="6dae1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6dae1-116">PARAMETERS</span></span>

### <span data-ttu-id="6dae1-117">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="6dae1-117">-Database</span></span>
<span data-ttu-id="6dae1-118">Bu cmdlet 'in aldığı kurtarılabilir veritabanını temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dae1-118">Specifies an object that represents the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dae1-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6dae1-119">-DatabaseName</span></span>
<span data-ttu-id="6dae1-120">Bu cmdlet 'in aldığı kurtarılabilir veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dae1-120">Specifies the name of the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dae1-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="6dae1-121">-Profile</span></span>
<span data-ttu-id="6dae1-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dae1-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6dae1-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="6dae1-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6dae1-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6dae1-124">-ServerName</span></span>
<span data-ttu-id="6dae1-125">Bu cmdlet 'in kurtarılabilir veritabanları aldığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dae1-125">Specifies the name of the server from which this cmdlet gets recoverable databases.</span></span>

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dae1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dae1-126">CommonParameters</span></span>
<span data-ttu-id="6dae1-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6dae1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dae1-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dae1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dae1-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6dae1-129">INPUTS</span></span>

### <span data-ttu-id="6dae1-130">Microsoft. Windowsazme. Management. Sql. modeller. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="6dae1-130">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="6dae1-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6dae1-131">OUTPUTS</span></span>

### <span data-ttu-id="6dae1-132">'A\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span><span class="sxs-lookup"><span data-stu-id="6dae1-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span></span>

## <span data-ttu-id="6dae1-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6dae1-133">NOTES</span></span>
* <span data-ttu-id="6dae1-134">Bu cmdlet 'i çalıştırmak için sertifika tabanlı kimlik doğrulaması kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="6dae1-134">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="6dae1-135">Bu cmdlet 'i çalıştıran bilgisayarda aşağıdaki komutları çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="6dae1-135">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="6dae1-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6dae1-136">RELATED LINKS</span></span>

[<span data-ttu-id="6dae1-137">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="6dae1-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="6dae1-138">Kurtarılabilir veritabanı</span><span class="sxs-lookup"><span data-stu-id="6dae1-138">Get Recoverable Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[<span data-ttu-id="6dae1-139">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="6dae1-139">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="6dae1-140">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="6dae1-140">Start-AzureSqlDatabaseRecovery</span></span>](./Start-AzureSqlDatabaseRecovery.md)


