---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5b75c2058fb7a6ddf323ebeaa6aad6967dcb5b01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758824"
---
# <span data-ttu-id="b5247-101">Remove-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b5247-101">Remove-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="b5247-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5247-102">SYNOPSIS</span></span>
<span data-ttu-id="b5247-103">Tehdit algılama ilkesini sunucudan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b5247-103">Removes the threat detection policy from a server.</span></span>

## <span data-ttu-id="b5247-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5247-104">SYNTAX</span></span>

```
Remove-AzSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5247-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5247-105">DESCRIPTION</span></span>
<span data-ttu-id="b5247-106">Remove-AzSqlServerThreatDetectionPolicy cmdlet 'i Azure SQL Server 'dan tehdit algılama ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b5247-106">The Remove-AzSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>
<span data-ttu-id="b5247-107">Bu cmdlet 'i kullanmak için, bu cmdlet 'in ilkeyi kaldırdığı sunucuyu belirlemek için ResourceGroupName ve ServerName parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b5247-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="b5247-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5247-108">EXAMPLES</span></span>

### <span data-ttu-id="b5247-109">Örnek 1: veritabanı için tehdit algılama ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="b5247-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\> Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="b5247-110">Bu komut, tehdit algılama ilkesini server01 adlı sunucudan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b5247-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="b5247-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5247-111">PARAMETERS</span></span>

### <span data-ttu-id="b5247-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5247-112">-DefaultProfile</span></span>
<span data-ttu-id="b5247-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b5247-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5247-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b5247-114">-PassThru</span></span>
<span data-ttu-id="b5247-115">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b5247-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b5247-116">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b5247-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b5247-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5247-117">-ResourceGroupName</span></span>
<span data-ttu-id="b5247-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5247-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="b5247-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b5247-119">-ServerName</span></span>
<span data-ttu-id="b5247-120">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5247-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="b5247-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5247-121">-Confirm</span></span>
<span data-ttu-id="b5247-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5247-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5247-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5247-123">-WhatIf</span></span>
<span data-ttu-id="b5247-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5247-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5247-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5247-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5247-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5247-126">CommonParameters</span></span>
<span data-ttu-id="b5247-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5247-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5247-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b5247-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5247-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5247-129">INPUTS</span></span>

### <span data-ttu-id="b5247-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b5247-130">System.String</span></span>

## <span data-ttu-id="b5247-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5247-131">OUTPUTS</span></span>

### <span data-ttu-id="b5247-132">Microsoft. Azure. Commands. Sql. ThreatDetection. model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b5247-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="b5247-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5247-133">NOTES</span></span>

## <span data-ttu-id="b5247-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5247-134">RELATED LINKS</span></span>

[<span data-ttu-id="b5247-135">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b5247-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

