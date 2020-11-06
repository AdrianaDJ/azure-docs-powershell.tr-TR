---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d59891980c11b90ee73275dbccb6a98b65c89613
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588028"
---
# <span data-ttu-id="f6366-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="f6366-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="f6366-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6366-102">SYNOPSIS</span></span>
<span data-ttu-id="f6366-103">Veritabanı için veri maskeleme ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f6366-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6366-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6366-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6366-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6366-105">DESCRIPTION</span></span>
<span data-ttu-id="f6366-106">**Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet 'i, BIR Azure SQL veritabanı için veri maskeleme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f6366-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="f6366-107">Bu cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f6366-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f6366-108">Veri maskeleme işlemlerinin etkin veya devre dışı olduğunu belirtmek için *Datamaskingstate* parametresini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6366-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="f6366-109">Ayrıca, maskelenmemiş verileri görmesine izin verilen kullanıcıları belirtmek için *Privilegevseçlogins* parametresini de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6366-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="f6366-110">Cmdlet başarılı olur ve *geçiş parametresi kullanılırsa* , veritabanı tanımlayıcılarına ek olarak geçerli veri maskeleme ilkesini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f6366-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="f6366-111">Veritabanı tanımlayıcıları, **Resourcegroupname** , **ServerName** ve **DatabaseName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="f6366-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="f6366-112">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="f6366-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f6366-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6366-113">EXAMPLES</span></span>

### <span data-ttu-id="f6366-114">Örnek 1: veritabanı için veri maskeleme ilkesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="f6366-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="f6366-115">Bu komut, server01 adındaki sunucudaki database01 adındaki veritabanı için veri maskeleme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f6366-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="f6366-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6366-116">PARAMETERS</span></span>

### <span data-ttu-id="f6366-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f6366-117">-DatabaseName</span></span>
<span data-ttu-id="f6366-118">İlkenin ayarlandığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6366-118">Specifies the name of the database where the policy is set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6366-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="f6366-119">-DataMaskingState</span></span>
<span data-ttu-id="f6366-120">Veri maskeleme işleminin etkin veya devre dışı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6366-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="f6366-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f6366-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6366-122">Etkin</span><span class="sxs-lookup"><span data-stu-id="f6366-122">Enabled</span></span>
- <span data-ttu-id="f6366-123">Devre dışı varsayılan değer etkindir.</span><span class="sxs-lookup"><span data-stu-id="f6366-123">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6366-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6366-124">-DefaultProfile</span></span>
<span data-ttu-id="f6366-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f6366-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6366-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f6366-126">-PassThru</span></span>
<span data-ttu-id="f6366-127">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f6366-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f6366-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="f6366-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6366-129">-Privilegevseçoturumlar</span><span class="sxs-lookup"><span data-stu-id="f6366-129">-PrivilegedLogins</span></span>
<span data-ttu-id="f6366-130">Hangi SQL kullanıcılarının maskeleme dışında tutulduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6366-130">Specifies which SQL users are excluded from masking.</span></span>
<span data-ttu-id="f6366-131">Bu parametre kullanım dışıdır ve ileriki sürümlerden kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="f6366-131">This parameter is deprecated and will be removed from future releases.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6366-132">-Privilegevseçusers</span><span class="sxs-lookup"><span data-stu-id="f6366-132">-PrivilegedUsers</span></span>
<span data-ttu-id="f6366-133">Ayrıcalıklı kullanıcı kimliklerinin noktalı virgülle ayrılmış listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6366-133">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="f6366-134">Bu kullanıcıların maskeleme verilerini görüntülemesine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="f6366-134">These users are allowed to view the masking data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6366-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6366-135">-ResourceGroupName</span></span>
<span data-ttu-id="f6366-136">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6366-136">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f6366-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f6366-137">-ServerName</span></span>
<span data-ttu-id="f6366-138">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6366-138">Specifies the name of the server hosting the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6366-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="f6366-139">-Confirm</span></span>
<span data-ttu-id="f6366-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f6366-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6366-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6366-141">-WhatIf</span></span>
<span data-ttu-id="f6366-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6366-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6366-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6366-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6366-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6366-144">CommonParameters</span></span>
<span data-ttu-id="f6366-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6366-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6366-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6366-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6366-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6366-147">INPUTS</span></span>

### <span data-ttu-id="f6366-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f6366-148">System.String</span></span>

## <span data-ttu-id="f6366-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6366-149">OUTPUTS</span></span>

### <span data-ttu-id="f6366-150">Microsoft. Azure. Commands. Sql. Datamaskeleme. model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f6366-150">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="f6366-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6366-151">NOTES</span></span>

## <span data-ttu-id="f6366-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6366-152">RELATED LINKS</span></span>

[<span data-ttu-id="f6366-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="f6366-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="f6366-154">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f6366-154">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f6366-155">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f6366-155">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f6366-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f6366-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f6366-157">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f6366-157">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f6366-158">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="f6366-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


