---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: ad64246d51e2f590ab19d93fd08fdd2a02943afd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763944"
---
# <span data-ttu-id="6ebb9-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="6ebb9-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="6ebb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ebb9-102">SYNOPSIS</span></span>
<span data-ttu-id="6ebb9-103">Azure SQL Server Danışmanı 'nın otomatik yürütme durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ebb9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ebb9-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ebb9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ebb9-105">DESCRIPTION</span></span>
<span data-ttu-id="6ebb9-106">**Set-Azurermsqlserverdanışmanlar Orautoexecutestatus** cmdlet 'ı BIR Azure SQL Server Danışmanı için otomatik yürütme özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-106">The **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="6ebb9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ebb9-107">EXAMPLES</span></span>

### <span data-ttu-id="6ebb9-108">Örnek 1: bir danışman için otomatik çalıştırmayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="6ebb9-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzureRmSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="6ebb9-109">Bu komut CreateIndex adındaki bir Advisor 'ın otomatik yürütme durumunu verir.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="6ebb9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ebb9-110">PARAMETERS</span></span>

### <span data-ttu-id="6ebb9-111">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="6ebb9-111">-AdvisorName</span></span>
<span data-ttu-id="6ebb9-112">Bu cmdlet 'in otomatik yürütme durumunu güncelleştirdiği bir danışman adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="6ebb9-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="6ebb9-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="6ebb9-114">Bu cmdlet 'in otomatik yürütme durumunu güncelleştirdiği değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="6ebb9-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6ebb9-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6ebb9-116">Etkin</span><span class="sxs-lookup"><span data-stu-id="6ebb9-116">Enabled</span></span>
- <span data-ttu-id="6ebb9-117">DISABLED</span><span class="sxs-lookup"><span data-stu-id="6ebb9-117">Disabled</span></span>
- <span data-ttu-id="6ebb9-118">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="6ebb9-118">Default</span></span>

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

### <span data-ttu-id="6ebb9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ebb9-119">-DefaultProfile</span></span>
<span data-ttu-id="6ebb9-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6ebb9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ebb9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ebb9-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ebb9-122">Sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="6ebb9-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6ebb9-123">-ServerName</span></span>
<span data-ttu-id="6ebb9-124">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="6ebb9-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ebb9-125">-Confirm</span></span>
<span data-ttu-id="6ebb9-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebb9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ebb9-127">-WhatIf</span></span>
<span data-ttu-id="6ebb9-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ebb9-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebb9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ebb9-130">CommonParameters</span></span>
<span data-ttu-id="6ebb9-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ebb9-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ebb9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ebb9-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ebb9-133">INPUTS</span></span>

### <span data-ttu-id="6ebb9-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6ebb9-134">None</span></span>
<span data-ttu-id="6ebb9-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ebb9-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ebb9-136">OUTPUTS</span></span>

### <span data-ttu-id="6ebb9-137">Microsoft. Azure. Commands. Sql. Advisor. model. Azuressqlserverdanışmanlar Ormodel</span><span class="sxs-lookup"><span data-stu-id="6ebb9-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="6ebb9-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ebb9-138">NOTES</span></span>
* <span data-ttu-id="6ebb9-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, Server, MSSQL, danışman</span><span class="sxs-lookup"><span data-stu-id="6ebb9-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="6ebb9-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ebb9-140">RELATED LINKS</span></span>

[<span data-ttu-id="6ebb9-141">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="6ebb9-141">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="6ebb9-142">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="6ebb9-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)