---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: d33635cd3876a3426c3db96489d623d0a61f1d03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592383"
---
# <span data-ttu-id="9f269-101">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="9f269-101">Start-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="9f269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f269-102">SYNOPSIS</span></span>
<span data-ttu-id="9f269-103">SQL veritabanı sunucusunu yükseltmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="9f269-103">Starts the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f269-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f269-104">SYNTAX</span></span>

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f269-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f269-105">DESCRIPTION</span></span>
<span data-ttu-id="9f269-106">**Start-AzureRmSqlServerUpgrade** cmdlet 'ı, Azure SQL veritabanı sunucusu sürüm 11 ' i sürüm 12 ' ye yükseltmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="9f269-106">The **Start-AzureRmSqlServerUpgrade** cmdlet starts the upgrade of an Azure SQL Database server version 11 to version 12.</span></span>
<span data-ttu-id="9f269-107">Get-AzureRmSqlServerUpgrade cmdlet 'ini kullanarak yükseltmenin ilerlemesini izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f269-107">You can monitor the progress of an upgrade by using the Get-AzureRmSqlServerUpgrade cmdlet.</span></span>

## <span data-ttu-id="9f269-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f269-108">EXAMPLES</span></span>

### <span data-ttu-id="9f269-109">Örnek 1: sunucuyu yükseltme</span><span class="sxs-lookup"><span data-stu-id="9f269-109">Example 1: Upgrade a server</span></span>
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

<span data-ttu-id="9f269-110">Bu komut, server01 adlı sunucuyu kaynak grubuna atanmış olarak yükseltir.</span><span class="sxs-lookup"><span data-stu-id="9f269-110">This command upgrades the server named server01 assigned to resource group TesourceGroup01.</span></span>

### <span data-ttu-id="9f269-111">Örnek 2: zamanlamayı zamanla ve veritabanı önerisi kullanarak sunucuyu yükseltme</span><span class="sxs-lookup"><span data-stu-id="9f269-111">Example 2: Upgrade a server by using schedule time and database recommendation</span></span>
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

<span data-ttu-id="9f269-112">İlk komut, Get-Date cmdlet 'ini kullanarak gelecekte beş dakikalık bir saat oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f269-112">The first command creates a time five minutes in the future by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="9f269-113">Komut $ScheduleTime değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="9f269-113">The command stores the date in the variable $ScheduleTime.</span></span>
<span data-ttu-id="9f269-114">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9f269-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="9f269-115">İkinci komut bir **RecommendedDatabaseProperties** nesnesi oluşturur ve bu nesneyi $DatabaseMap değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="9f269-115">The second command creates a **RecommendedDatabaseProperties** object, and then stores that object in the variable $DatabaseMap.</span></span>

<span data-ttu-id="9f269-116">Sonraki üç komut, $DatabaseMap depolanan nesnenin özelliklerine değerler atar.</span><span class="sxs-lookup"><span data-stu-id="9f269-116">The next three commands assign values to properties of the object stored in $DatabaseMap.</span></span>

<span data-ttu-id="9f269-117">Son komut, server01 adındaki var olan sunucuyu 12,0 sürümüne yükseltir.</span><span class="sxs-lookup"><span data-stu-id="9f269-117">The final command upgrades the existing server named Server01 to version 12.0.</span></span>
<span data-ttu-id="9f269-118">$ScheduleTime değişkeninde belirtildiği gibi, komutu çalıştırdıktan sonraki en erken saat beş dakikadır.</span><span class="sxs-lookup"><span data-stu-id="9f269-118">The earliest time to upgrade is five minutes after you run the command, as specified by the $ScheduleTime variable.</span></span>
<span data-ttu-id="9f269-119">Yükseltmenin ardından, veritabanı contosodb standart sürümü çalıştırmaya başlar ve hizmet düzeyi amacını S0 olur.</span><span class="sxs-lookup"><span data-stu-id="9f269-119">After the upgrade, the database contosodb will be running the Standard edition and have the Service Level Objective S0.</span></span>

## <span data-ttu-id="9f269-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f269-120">PARAMETERS</span></span>

### <span data-ttu-id="9f269-121">-DatabaseCollection</span><span class="sxs-lookup"><span data-stu-id="9f269-121">-DatabaseCollection</span></span>
<span data-ttu-id="9f269-122">Bu cmdlet 'in sunucu yükseltmesinde kullandığı bir **RecommendedDatabaseProperties** nesneleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f269-122">Specifies an array of **RecommendedDatabaseProperties** objects that this cmdlet uses for the server upgrade.</span></span>

```yaml
Type: RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f269-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f269-123">-DefaultProfile</span></span>
<span data-ttu-id="9f269-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9f269-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f269-125">-Elaafcollection</span><span class="sxs-lookup"><span data-stu-id="9f269-125">-ElasticPoolCollection</span></span>
<span data-ttu-id="9f269-126">Sunucu yükseltmesinde kullanılacak bir **yükseltilebilir Dereyorumdedelaçıkartpoolproperties** nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f269-126">Specifies an array of **UpgradeRecommendedElasticPoolProperties** objects to use for the server upgrade.</span></span>

```yaml
Type: UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f269-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f269-127">-ResourceGroupName</span></span>
<span data-ttu-id="9f269-128">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f269-128">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f269-129">-ScheduleUpgradeAfterUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="9f269-129">-ScheduleUpgradeAfterUtcDateTime</span></span>
<span data-ttu-id="9f269-130">Sunucuyu yükseltebileceğiniz en erken zamanı bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f269-130">Specifies the earliest time, as a **DateTime** object, to upgrade the server.</span></span>
<span data-ttu-id="9f269-131">ISO8601 biçiminde, Eşgüdümlü Evrensel Saat (UTC) cinsinden bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="9f269-131">Specify a value in the ISO8601 format, in Coordinated Universal Time (UTC).</span></span>
<span data-ttu-id="9f269-132">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9f269-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f269-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9f269-133">-ServerName</span></span>
<span data-ttu-id="9f269-134">Bu cmdlet 'in yükselttiğinde sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f269-134">Specifies the name of the server that this cmdlet upgrades.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f269-135">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="9f269-135">-ServerVersion</span></span>
<span data-ttu-id="9f269-136">Bu cmdlet 'in sunucuyu yükselttiğinde sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f269-136">Specifies the version to which this cmdlet upgrades the server.</span></span>
<span data-ttu-id="9f269-137">Geçerli tek değer 12,0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="9f269-137">The only valid value is 12.0.</span></span>

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

### <span data-ttu-id="9f269-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f269-138">CommonParameters</span></span>
<span data-ttu-id="9f269-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f269-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f269-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f269-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f269-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f269-141">INPUTS</span></span>

### <span data-ttu-id="9f269-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9f269-142">None</span></span>
<span data-ttu-id="9f269-143">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9f269-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9f269-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f269-144">OUTPUTS</span></span>

### <span data-ttu-id="9f269-145">Microsoft. Azure. Commands. Sql. ServerUpgrade. model. azures, Serverupgrademodel</span><span class="sxs-lookup"><span data-stu-id="9f269-145">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="9f269-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f269-146">NOTES</span></span>

## <span data-ttu-id="9f269-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f269-147">RELATED LINKS</span></span>

[<span data-ttu-id="9f269-148">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="9f269-148">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="9f269-149">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="9f269-149">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="9f269-150">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="9f269-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


