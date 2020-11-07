---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: b0ca96910d763cfcf40530ad99872e1e0d50ca31
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758851"
---
# <span data-ttu-id="45a93-101">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="45a93-101">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="45a93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45a93-102">SYNOPSIS</span></span>
<span data-ttu-id="45a93-103">Tehdit algılama ilkesini veritabanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="45a93-103">Removes the threat detection policy from a database.</span></span>

## <span data-ttu-id="45a93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45a93-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45a93-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45a93-105">DESCRIPTION</span></span>
<span data-ttu-id="45a93-106">**Remove-AzSqlDatabaseThreatDetectionPolicy** cmdlet 'i, tehdit algılama Ilkesini Azureazma SQL veritabanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="45a93-106">The **Remove-AzSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="45a93-107">Bu cmdlet 'i kullanmak için, bu cmdlet 'in ilkeyi kaldırdığı veritabanını tanımlamak için *Resourcegroupname* ve *ServerName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="45a93-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="45a93-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45a93-108">EXAMPLES</span></span>

### <span data-ttu-id="45a93-109">Örnek 1: veritabanı için tehdit algılama ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="45a93-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="45a93-110">Bu komut, server01 adındaki sunucudaki Database01 adlı veritabanından tehdit algılama ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="45a93-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="45a93-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45a93-111">PARAMETERS</span></span>

### <span data-ttu-id="45a93-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="45a93-112">-DatabaseName</span></span>
<span data-ttu-id="45a93-113">Tehdit algılama ilkesinin kaldırılması gereken veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45a93-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

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

### <span data-ttu-id="45a93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a93-114">-DefaultProfile</span></span>
<span data-ttu-id="45a93-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="45a93-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a93-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="45a93-116">-PassThru</span></span>
<span data-ttu-id="45a93-117">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="45a93-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="45a93-118">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="45a93-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="45a93-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45a93-119">-ResourceGroupName</span></span>
<span data-ttu-id="45a93-120">Sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45a93-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="45a93-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="45a93-121">-ServerName</span></span>
<span data-ttu-id="45a93-122">Veritabanının çalıştığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45a93-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="45a93-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="45a93-123">-Confirm</span></span>
<span data-ttu-id="45a93-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="45a93-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45a93-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45a93-125">-WhatIf</span></span>
<span data-ttu-id="45a93-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="45a93-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45a93-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="45a93-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45a93-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a93-128">CommonParameters</span></span>
<span data-ttu-id="45a93-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45a93-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a93-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="45a93-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a93-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45a93-131">INPUTS</span></span>

### <span data-ttu-id="45a93-132">System. String</span><span class="sxs-lookup"><span data-stu-id="45a93-132">System.String</span></span>

## <span data-ttu-id="45a93-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45a93-133">OUTPUTS</span></span>

### <span data-ttu-id="45a93-134">Microsoft. Azure. Commands. Sql. ThreatDetection. model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="45a93-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="45a93-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45a93-135">NOTES</span></span>

## <span data-ttu-id="45a93-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45a93-136">RELATED LINKS</span></span>

[<span data-ttu-id="45a93-137">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="45a93-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


