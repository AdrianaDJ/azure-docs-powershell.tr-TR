---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 972F4188-52C5-4B92-8B88-E68526537F48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 692c4fd98db0ebaff70e740abc8a7238e4a28685
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762438"
---
# <span data-ttu-id="78f75-101">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="78f75-101">Stop-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="78f75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78f75-102">SYNOPSIS</span></span>
<span data-ttu-id="78f75-103">SQL veritabanı sunucusunu yükseltmeyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="78f75-103">Stops the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78f75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78f75-104">SYNTAX</span></span>

```
Stop-AzureRmSqlServerUpgrade [-Force] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78f75-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="78f75-105">DESCRIPTION</span></span>
<span data-ttu-id="78f75-106">**Stop-AzureRmSqlServerUpgrade** cmdlet 'ı BIR Azure SQL veritabanı sunucusunun yükseltmesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="78f75-106">The **Stop-AzureRmSqlServerUpgrade** cmdlet stops the upgrade of an Azure SQL Database server.</span></span>

## <span data-ttu-id="78f75-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78f75-107">EXAMPLES</span></span>

### <span data-ttu-id="78f75-108">Örnek 1: sunucu yükseltmesini durdurma</span><span class="sxs-lookup"><span data-stu-id="78f75-108">Example 1: Stop a server upgrade</span></span>
```
PS C:\>Stop-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server02"
```

<span data-ttu-id="78f75-109">Bu komut, ResourceGroup01 adındaki kaynak grubuna atanmış Server02 adlı sunucuyu yükseltme isteğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="78f75-109">This command stops the request to upgrade the server named Server02 assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="78f75-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78f75-110">PARAMETERS</span></span>

### <span data-ttu-id="78f75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f75-111">-DefaultProfile</span></span>
<span data-ttu-id="78f75-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="78f75-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78f75-113">-Force</span><span class="sxs-lookup"><span data-stu-id="78f75-113">-Force</span></span>
<span data-ttu-id="78f75-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="78f75-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="78f75-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f75-115">-ResourceGroupName</span></span>
<span data-ttu-id="78f75-116">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78f75-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="78f75-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="78f75-117">-ServerName</span></span>
<span data-ttu-id="78f75-118">Bu cmdlet 'in yükseltmeyi durdurduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78f75-118">Specifies the name of the server for which this cmdlet stops an upgrade.</span></span>

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

### <span data-ttu-id="78f75-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="78f75-119">-Confirm</span></span>
<span data-ttu-id="78f75-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="78f75-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f75-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f75-121">-WhatIf</span></span>
<span data-ttu-id="78f75-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="78f75-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78f75-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="78f75-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78f75-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f75-124">CommonParameters</span></span>
<span data-ttu-id="78f75-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78f75-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f75-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78f75-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f75-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78f75-127">INPUTS</span></span>

### <span data-ttu-id="78f75-128">System. String</span><span class="sxs-lookup"><span data-stu-id="78f75-128">System.String</span></span>

## <span data-ttu-id="78f75-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78f75-129">OUTPUTS</span></span>

### <span data-ttu-id="78f75-130">Microsoft. Azure. Commands. Sql. ServerUpgrade. model. azures, Serverupgrademodel</span><span class="sxs-lookup"><span data-stu-id="78f75-130">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="78f75-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78f75-131">NOTES</span></span>

## <span data-ttu-id="78f75-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78f75-132">RELATED LINKS</span></span>

[<span data-ttu-id="78f75-133">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="78f75-133">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="78f75-134">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="78f75-134">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="78f75-135">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="78f75-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


