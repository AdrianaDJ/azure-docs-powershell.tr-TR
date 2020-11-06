---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: d2a92e7209745873364b5de114916bc48b0a3b42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587766"
---
# <span data-ttu-id="20059-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="20059-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="20059-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20059-102">SYNOPSIS</span></span>
<span data-ttu-id="20059-103">Azure SQL veritabanı sunucusu yükseltmesinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="20059-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20059-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20059-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20059-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="20059-105">DESCRIPTION</span></span>
<span data-ttu-id="20059-106">**Get-AzureRmSqlServerUpgrade** cmdlet 'ı, Azure SQL veritabanı sunucusu yükseltmesinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="20059-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="20059-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20059-107">EXAMPLES</span></span>

### <span data-ttu-id="20059-108">Örnek 1: yükseltme durumunu alma</span><span class="sxs-lookup"><span data-stu-id="20059-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="20059-109">Bu komut, ResourceGroup01 adındaki kaynak grubundaki server01 adındaki sunucudan yükseltme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="20059-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="20059-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20059-110">PARAMETERS</span></span>

### <span data-ttu-id="20059-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20059-111">-ResourceGroupName</span></span>
<span data-ttu-id="20059-112">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20059-112">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="20059-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="20059-113">-ServerName</span></span>
<span data-ttu-id="20059-114">Bu cmdlet 'in yükseltme durumunu aldığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20059-114">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

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

### <span data-ttu-id="20059-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="20059-115">-Confirm</span></span>
<span data-ttu-id="20059-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="20059-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20059-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20059-117">-WhatIf</span></span>
<span data-ttu-id="20059-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="20059-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20059-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="20059-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20059-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20059-120">-DefaultProfile</span></span>
<span data-ttu-id="20059-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20059-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20059-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20059-122">CommonParameters</span></span>
<span data-ttu-id="20059-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20059-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20059-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20059-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20059-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20059-125">INPUTS</span></span>

## <span data-ttu-id="20059-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20059-126">OUTPUTS</span></span>

### <span data-ttu-id="20059-127">Microsoft. Azure. Commands. Sql. ServerUpgrade. model. azures, Serverupgrademodel</span><span class="sxs-lookup"><span data-stu-id="20059-127">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="20059-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20059-128">NOTES</span></span>

## <span data-ttu-id="20059-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20059-129">RELATED LINKS</span></span>

[<span data-ttu-id="20059-130">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="20059-130">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="20059-131">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="20059-131">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="20059-132">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="20059-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


