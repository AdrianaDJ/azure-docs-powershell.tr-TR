---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 8860b4952f11e1d0ad07ca65e6ed77f8fdc2fa5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758886"
---
# <span data-ttu-id="d6a5a-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d6a5a-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="d6a5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a5a-103">İki SQL veritabanı sunucusu arasındaki elastik veritabanı işlemleri için iletişim bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="d6a5a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6a5a-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6a5a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="d6a5a-106">**New-AzSqlServerCommunicationLink** cmdlet 'ı, Azure SQL veritabanındaki iki mantıksal sunucu arasındaki elastik veritabanı işlemleri için iletişim bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="d6a5a-107">Elastik veritabanı işlemleri eşlenmiş sunuculardan herhangi birinin veritabanına yayılabilir.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="d6a5a-108">Bir sunucuda birden çok bağlantı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="d6a5a-109">Bu nedenle, elastik veritabanı işlemleri daha fazla sayıda sunucuya yayılabilir.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="d6a5a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6a5a-110">EXAMPLES</span></span>

### <span data-ttu-id="d6a5a-111">Örnek 1: iletişim bağlantısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="d6a5a-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="d6a5a-112">Bu komut ContosoServer17 ve ContosoServer02 arasında Link01 adlı bir bağlantı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="d6a5a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6a5a-113">PARAMETERS</span></span>

### <span data-ttu-id="d6a5a-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="d6a5a-114">-AsJob</span></span>
<span data-ttu-id="d6a5a-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d6a5a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6a5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a5a-116">-DefaultProfile</span></span>
<span data-ttu-id="d6a5a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d6a5a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6a5a-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="d6a5a-118">-LinkName</span></span>
<span data-ttu-id="d6a5a-119">Bu cmdlet 'in oluşturduğu sunucu iletişim bağlantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a5a-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="d6a5a-120">-PartnerServer</span></span>
<span data-ttu-id="d6a5a-121">Bu iletişim bağlantısında yer alan diğer sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-121">Specifies the name of the other server that takes part in this communication link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a5a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a5a-122">-ResourceGroupName</span></span>
<span data-ttu-id="d6a5a-123">*ServerName* parametresi tarafından belirtilen sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="d6a5a-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d6a5a-124">-ServerName</span></span>
<span data-ttu-id="d6a5a-125">Bu cmdlet 'in iletişim bağlantısını ayarladığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="d6a5a-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="d6a5a-126">-Confirm</span></span>
<span data-ttu-id="d6a5a-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6a5a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6a5a-128">-WhatIf</span></span>
<span data-ttu-id="d6a5a-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6a5a-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6a5a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a5a-131">CommonParameters</span></span>
<span data-ttu-id="d6a5a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a5a-133">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d6a5a-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a5a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6a5a-134">INPUTS</span></span>

### <span data-ttu-id="d6a5a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d6a5a-135">System.String</span></span>

## <span data-ttu-id="d6a5a-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6a5a-136">OUTPUTS</span></span>

### <span data-ttu-id="d6a5a-137">Microsoft. Azure. Commands. Sql. ServerCommunicationLink. model. Azuressqlservercommunicationlinkmodel</span><span class="sxs-lookup"><span data-stu-id="d6a5a-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="d6a5a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6a5a-138">NOTES</span></span>
* <span data-ttu-id="d6a5a-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="d6a5a-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="d6a5a-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6a5a-140">RELATED LINKS</span></span>

[<span data-ttu-id="d6a5a-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d6a5a-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="d6a5a-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d6a5a-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="d6a5a-143">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="d6a5a-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)