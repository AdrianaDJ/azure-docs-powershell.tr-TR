---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: e37a825a2da5f922a9a8a31bcc7f15a78f7cc38b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588035"
---
# <span data-ttu-id="16593-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="16593-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="16593-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16593-102">SYNOPSIS</span></span>
<span data-ttu-id="16593-103">Azure SQL veritabanı Danışmanı 'nın otomatik yürütme durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="16593-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16593-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16593-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16593-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="16593-105">DESCRIPTION</span></span>
<span data-ttu-id="16593-106">**Set-Azurermsqldatabasedanışmanlar Orautoexecutestatus** cmdlet 'ı, Azure SQL veritabanı Danışmanı 'nın otomatik yürütme özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="16593-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="16593-107">Şu anda bu cmdlet Enabled, Disabled ve default değerlerini destekler.</span><span class="sxs-lookup"><span data-stu-id="16593-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="16593-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16593-108">EXAMPLES</span></span>

### <span data-ttu-id="16593-109">Örnek 1: bir danışman için otomatik çalıştırmayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="16593-109">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="16593-110">Bu komut, CreateIndex adındaki bir Advisor 'ın otomatik yürütme durumunu etkin olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="16593-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="16593-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16593-111">PARAMETERS</span></span>

### <span data-ttu-id="16593-112">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="16593-112">-AdvisorName</span></span>
<span data-ttu-id="16593-113">Bu cmdlet 'in durumu değiştirdiği danışman adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16593-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16593-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="16593-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="16593-115">Durumun değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="16593-115">Specifies the value for the status.</span></span>
<span data-ttu-id="16593-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="16593-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16593-117">Etkin</span><span class="sxs-lookup"><span data-stu-id="16593-117">Enabled</span></span> 
- <span data-ttu-id="16593-118">DISABLED</span><span class="sxs-lookup"><span data-stu-id="16593-118">Disabled</span></span> 
- <span data-ttu-id="16593-119">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="16593-119">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16593-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16593-120">-DatabaseName</span></span>
<span data-ttu-id="16593-121">Bu cmdlet 'in durumu değiştirdiği veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16593-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16593-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16593-122">-DefaultProfile</span></span>
<span data-ttu-id="16593-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="16593-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16593-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16593-124">-ResourceGroupName</span></span>
<span data-ttu-id="16593-125">Bu veritabanını içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16593-125">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16593-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="16593-126">-ServerName</span></span>
<span data-ttu-id="16593-127">Veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16593-127">Specifies the name of the server for the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16593-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="16593-128">-Confirm</span></span>
<span data-ttu-id="16593-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16593-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16593-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16593-130">-WhatIf</span></span>
<span data-ttu-id="16593-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16593-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16593-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16593-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16593-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16593-133">CommonParameters</span></span>
<span data-ttu-id="16593-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16593-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16593-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16593-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16593-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16593-136">INPUTS</span></span>

### <span data-ttu-id="16593-137">System. String</span><span class="sxs-lookup"><span data-stu-id="16593-137">System.String</span></span>

### <span data-ttu-id="16593-138">Microsoft. Azure. Commands. Sql. Advisor. cmdlet. danışmanlar Orautoexecutestatus</span><span class="sxs-lookup"><span data-stu-id="16593-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="16593-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16593-139">OUTPUTS</span></span>

### <span data-ttu-id="16593-140">Microsoft. Azure. Commands. Sql. Advisor. model. Azuressqldatabasedanışmanlar Ormodel</span><span class="sxs-lookup"><span data-stu-id="16593-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="16593-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16593-141">NOTES</span></span>

## <span data-ttu-id="16593-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16593-142">RELATED LINKS</span></span>

[<span data-ttu-id="16593-143">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="16593-143">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="16593-144">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="16593-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

