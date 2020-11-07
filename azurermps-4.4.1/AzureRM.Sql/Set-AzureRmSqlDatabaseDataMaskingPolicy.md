---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 72ee5f7bd636747b4321e1c87b78fdb37ed84dc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762675"
---
# <span data-ttu-id="260ac-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="260ac-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="260ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="260ac-102">SYNOPSIS</span></span>
<span data-ttu-id="260ac-103">Veritabanı için veri maskeleme ayarlar.</span><span class="sxs-lookup"><span data-stu-id="260ac-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="260ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="260ac-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="260ac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="260ac-105">DESCRIPTION</span></span>
<span data-ttu-id="260ac-106">**Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet 'i, BIR Azure SQL veritabanı için veri maskeleme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="260ac-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="260ac-107">Bu cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="260ac-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="260ac-108">Veri maskeleme işlemlerinin etkin veya devre dışı olduğunu belirtmek için *Datamaskingstate* parametresini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="260ac-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>

<span data-ttu-id="260ac-109">Ayrıca, maskelenmemiş verileri görmesine izin verilen kullanıcıları belirtmek için *Privilegevseçlogins* parametresini de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="260ac-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="260ac-110">Cmdlet başarılı olur ve *geçiş parametresi kullanılırsa* , veritabanı tanımlayıcılarına ek olarak geçerli veri maskeleme ilkesini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="260ac-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="260ac-111">Veritabanı tanımlayıcıları, **Resourcegroupname** , **ServerName** ve **DatabaseName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="260ac-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="260ac-112">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="260ac-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="260ac-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="260ac-113">EXAMPLES</span></span>

### <span data-ttu-id="260ac-114">Örnek 1: veritabanı için veri maskeleme ilkesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="260ac-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="260ac-115">Bu komut, server01 adındaki sunucudaki database01 adındaki veritabanı için veri maskeleme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="260ac-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="260ac-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="260ac-116">PARAMETERS</span></span>

### <span data-ttu-id="260ac-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="260ac-117">-DatabaseName</span></span>
<span data-ttu-id="260ac-118">İlkenin ayarlandığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="260ac-118">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="260ac-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="260ac-119">-DataMaskingState</span></span>
<span data-ttu-id="260ac-120">Veri maskeleme işleminin etkin veya devre dışı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="260ac-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="260ac-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="260ac-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="260ac-122">Etkin</span><span class="sxs-lookup"><span data-stu-id="260ac-122">Enabled</span></span>
- <span data-ttu-id="260ac-123">DISABLED</span><span class="sxs-lookup"><span data-stu-id="260ac-123">Disabled</span></span>

<span data-ttu-id="260ac-124">Varsayılan değer etkindir.</span><span class="sxs-lookup"><span data-stu-id="260ac-124">The default value is Enabled.</span></span>

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

### <span data-ttu-id="260ac-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="260ac-125">-PassThru</span></span>
<span data-ttu-id="260ac-126">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="260ac-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="260ac-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="260ac-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="260ac-128">-Privilegevseçoturumlar</span><span class="sxs-lookup"><span data-stu-id="260ac-128">-PrivilegedLogins</span></span>
<span data-ttu-id="260ac-129">Hangi SQL kullanıcılarının maskeleme dışında tutulduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="260ac-129">Specifies which SQL users are excluded from masking.</span></span>

<span data-ttu-id="260ac-130">Bu parametre kullanım dışıdır ve ileriki sürümlerden kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="260ac-130">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="260ac-131">-Privilegevseçusers</span><span class="sxs-lookup"><span data-stu-id="260ac-131">-PrivilegedUsers</span></span>
<span data-ttu-id="260ac-132">Ayrıcalıklı kullanıcı kimliklerinin noktalı virgülle ayrılmış listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="260ac-132">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="260ac-133">Bu kullanıcıların maskeleme verilerini görüntülemesine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="260ac-133">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="260ac-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="260ac-134">-ResourceGroupName</span></span>
<span data-ttu-id="260ac-135">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="260ac-135">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="260ac-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="260ac-136">-ServerName</span></span>
<span data-ttu-id="260ac-137">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="260ac-137">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="260ac-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="260ac-138">-Confirm</span></span>
<span data-ttu-id="260ac-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="260ac-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="260ac-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="260ac-140">-WhatIf</span></span>
<span data-ttu-id="260ac-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="260ac-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="260ac-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="260ac-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="260ac-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="260ac-143">-DefaultProfile</span></span>
<span data-ttu-id="260ac-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="260ac-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="260ac-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="260ac-145">CommonParameters</span></span>
<span data-ttu-id="260ac-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="260ac-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="260ac-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="260ac-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="260ac-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="260ac-148">INPUTS</span></span>

## <span data-ttu-id="260ac-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="260ac-149">OUTPUTS</span></span>

### <span data-ttu-id="260ac-150">Microsoft. Azure. Commands. Sql. Security. model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="260ac-150">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="260ac-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="260ac-151">NOTES</span></span>

## <span data-ttu-id="260ac-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="260ac-152">RELATED LINKS</span></span>

[<span data-ttu-id="260ac-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="260ac-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="260ac-154">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="260ac-154">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="260ac-155">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="260ac-155">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="260ac-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="260ac-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="260ac-157">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="260ac-157">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="260ac-158">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="260ac-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


