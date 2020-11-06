---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 976dbc06c71b31ea9058355d55f1eff53681f6e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592721"
---
# <span data-ttu-id="9c850-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="9c850-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="9c850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c850-102">SYNOPSIS</span></span>
<span data-ttu-id="9c850-103">Bir veritabanının Thal durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="9c850-103">Gets the TDE state for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c850-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c850-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c850-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c850-105">DESCRIPTION</span></span>
<span data-ttu-id="9c850-106">**Get-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet 'i, BIR Azure SQL veritabanı Için saydam veri şifrelemesi (tde) durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="9c850-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="9c850-107">Daha fazla bilgi için, Azure SQL veritabanıyla https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) Microsoft Developer Network Library) saydam veri şifrelemesi konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="9c850-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="9c850-108">Bu cmdlet TDE 'in geçerli durumunu alır, ancak şifreleme ve şifre çözme uzun süren işlemler olabilir.</span><span class="sxs-lookup"><span data-stu-id="9c850-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="9c850-109">Şifreleme taraması ilerleme durumunu görmek için Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="9c850-109">To see the encryption scan progress, run the Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="9c850-110">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="9c850-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="9c850-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c850-111">EXAMPLES</span></span>

### <span data-ttu-id="9c850-112">Örnek 1: veritabanı için ton durumunu alma</span><span class="sxs-lookup"><span data-stu-id="9c850-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="9c850-113">Bu komut, server01 adındaki sunucudaki Database01 adlı veritabanı için ton durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="9c850-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="9c850-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c850-114">PARAMETERS</span></span>

### <span data-ttu-id="9c850-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9c850-115">-DatabaseName</span></span>
<span data-ttu-id="9c850-116">Bu cmdlet 'in TDA durumu aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c850-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="9c850-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c850-117">-DefaultProfile</span></span>
<span data-ttu-id="9c850-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9c850-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c850-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c850-119">-ResourceGroupName</span></span>
<span data-ttu-id="9c850-120">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c850-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="9c850-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9c850-121">-ServerName</span></span>
<span data-ttu-id="9c850-122">Bu cmdlet 'in TDA durumunu aldığı veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c850-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="9c850-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="9c850-123">-Confirm</span></span>
<span data-ttu-id="9c850-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9c850-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c850-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c850-125">-WhatIf</span></span>
<span data-ttu-id="9c850-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c850-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c850-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9c850-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c850-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c850-128">CommonParameters</span></span>
<span data-ttu-id="9c850-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c850-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c850-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c850-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c850-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c850-131">INPUTS</span></span>

### <span data-ttu-id="9c850-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9c850-132">System.String</span></span>

## <span data-ttu-id="9c850-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c850-133">OUTPUTS</span></span>

### <span data-ttu-id="9c850-134">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="9c850-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="9c850-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c850-135">NOTES</span></span>

## <span data-ttu-id="9c850-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c850-136">RELATED LINKS</span></span>

[<span data-ttu-id="9c850-137">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="9c850-137">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="9c850-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="9c850-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)
