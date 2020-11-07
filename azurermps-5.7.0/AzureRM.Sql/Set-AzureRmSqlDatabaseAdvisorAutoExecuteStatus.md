---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 7af5736e2f66b8bf428815456ba95b3c5b4b6182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762342"
---
# <span data-ttu-id="f3ae4-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f3ae4-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="f3ae4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ae4-103">Azure SQL veritabanı Danışmanı 'nın otomatik yürütme durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3ae4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3ae4-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3ae4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3ae4-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ae4-106">**Set-Azurermsqldatabasedanışmanlar Orautoexecutestatus** cmdlet 'ı, Azure SQL veritabanı Danışmanı 'nın otomatik yürütme özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="f3ae4-107">Şu anda bu cmdlet Enabled, Disabled ve default değerlerini destekler.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="f3ae4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3ae4-108">EXAMPLES</span></span>

### <span data-ttu-id="f3ae4-109">Örnek 1: bir danışman için otomatik çalıştırmayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f3ae4-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="f3ae4-110">Bu komut, CreateIndex adındaki bir Advisor 'ın otomatik yürütme durumunu etkin olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="f3ae4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3ae4-111">PARAMETERS</span></span>

### <span data-ttu-id="f3ae4-112">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="f3ae4-112">-AdvisorName</span></span>
<span data-ttu-id="f3ae4-113">Bu cmdlet 'in durumu değiştirdiği danışman adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="f3ae4-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f3ae4-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="f3ae4-115">Durumun değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-115">Specifies the value for the status.</span></span>
<span data-ttu-id="f3ae4-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f3ae4-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3ae4-117">Etkin</span><span class="sxs-lookup"><span data-stu-id="f3ae4-117">Enabled</span></span> 
- <span data-ttu-id="f3ae4-118">DISABLED</span><span class="sxs-lookup"><span data-stu-id="f3ae4-118">Disabled</span></span> 
- <span data-ttu-id="f3ae4-119">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="f3ae4-119">Default</span></span>

```yaml
Type: AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ae4-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f3ae4-120">-DatabaseName</span></span>
<span data-ttu-id="f3ae4-121">Bu cmdlet 'in durumu değiştirdiği veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="f3ae4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ae4-122">-DefaultProfile</span></span>
<span data-ttu-id="f3ae4-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f3ae4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3ae4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ae4-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3ae4-125">Bu veritabanını içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="f3ae4-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f3ae4-126">-ServerName</span></span>
<span data-ttu-id="f3ae4-127">Veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="f3ae4-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="f3ae4-128">-Confirm</span></span>
<span data-ttu-id="f3ae4-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ae4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3ae4-130">-WhatIf</span></span>
<span data-ttu-id="f3ae4-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3ae4-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ae4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ae4-133">CommonParameters</span></span>
<span data-ttu-id="f3ae4-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ae4-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ae4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ae4-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3ae4-136">INPUTS</span></span>

### <span data-ttu-id="f3ae4-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f3ae4-137">None</span></span>
<span data-ttu-id="f3ae4-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3ae4-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3ae4-139">OUTPUTS</span></span>

### <span data-ttu-id="f3ae4-140">Microsoft. Azure. Commands. Sql. Advisor. model. Azuressqldatabasedanışmanlar Ormodel</span><span class="sxs-lookup"><span data-stu-id="f3ae4-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>
<span data-ttu-id="f3ae4-141">Bu cmdlet bir **Azuressqldatabasedanışmanlar Ormodel** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="f3ae4-141">This cmdlet returns an **AzureSqlDatabaseAdvisorModel** object.</span></span>

## <span data-ttu-id="f3ae4-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3ae4-142">NOTES</span></span>

## <span data-ttu-id="f3ae4-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3ae4-143">RELATED LINKS</span></span>

[<span data-ttu-id="f3ae4-144">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="f3ae4-144">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="f3ae4-145">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="f3ae4-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

