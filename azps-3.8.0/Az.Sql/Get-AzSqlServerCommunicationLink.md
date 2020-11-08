---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096061"
---
# <span data-ttu-id="f4be0-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="f4be0-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="f4be0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4be0-102">SYNOPSIS</span></span>
<span data-ttu-id="f4be0-103">Veritabanı sunucuları arasındaki elastik veritabanı işlemleri için iletişim bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f4be0-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="f4be0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4be0-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4be0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4be0-105">DESCRIPTION</span></span>
<span data-ttu-id="f4be0-106">**Get-AzSqlServerCommunicationLink** cmdlet 'ı, Azure SQL veritabanındaki elastik veritabanı işlemleri için sunucudan sunucuya iletişim bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f4be0-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="f4be0-107">Bağlantının özelliklerini görmek için sunucu iletişim bağlantısının adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="f4be0-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="f4be0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4be0-108">EXAMPLES</span></span>

### <span data-ttu-id="f4be0-109">Örnek 1: sunucunun tüm iletişim bağlantılarını alma</span><span class="sxs-lookup"><span data-stu-id="f4be0-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="f4be0-110">Bu komut, ContosoServer17 adlı sunucudaki elastik veritabanı işlemleri için tüm sunucudan sunucuya iletişim bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f4be0-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="f4be0-111">Örnek 2: sunucu için belirli bir iletişim bağlantısı alma</span><span class="sxs-lookup"><span data-stu-id="f4be0-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="f4be0-112">Bu komut, Link01 adlı sunucudan sunucuya iletişim bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="f4be0-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="f4be0-113">Örnek 3: filtreleme kullanarak sunucunun tüm iletişim bağlantılarını alma</span><span class="sxs-lookup"><span data-stu-id="f4be0-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="f4be0-114">Bu komut, "LINK" ile başlayan ContosoServer17 adlı sunucudaki elastik veritabanı işlemleri için tüm sunucudan sunucuya iletişim bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f4be0-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="f4be0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4be0-115">PARAMETERS</span></span>

### <span data-ttu-id="f4be0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4be0-116">-DefaultProfile</span></span>
<span data-ttu-id="f4be0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f4be0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4be0-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="f4be0-118">-LinkName</span></span>
<span data-ttu-id="f4be0-119">Bu cmdlet 'in aldığı sunucu iletişim bağlantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4be0-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4be0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4be0-120">-ResourceGroupName</span></span>
<span data-ttu-id="f4be0-121">*ServerName* parametresi tarafından belirtilen sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4be0-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="f4be0-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f4be0-122">-ServerName</span></span>
<span data-ttu-id="f4be0-123">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4be0-123">Specifies the name of a server.</span></span>
<span data-ttu-id="f4be0-124">Bu sunucu, bu cmdlet 'in aldığı iletişim bağlantısını içerir.</span><span class="sxs-lookup"><span data-stu-id="f4be0-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f4be0-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="f4be0-125">-Confirm</span></span>
<span data-ttu-id="f4be0-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f4be0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4be0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4be0-127">-WhatIf</span></span>
<span data-ttu-id="f4be0-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4be0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4be0-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f4be0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4be0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4be0-130">CommonParameters</span></span>
<span data-ttu-id="f4be0-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4be0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4be0-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f4be0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4be0-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4be0-133">INPUTS</span></span>

### <span data-ttu-id="f4be0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f4be0-134">System.String</span></span>

## <span data-ttu-id="f4be0-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4be0-135">OUTPUTS</span></span>

### <span data-ttu-id="f4be0-136">Microsoft. Azure. Commands. Sql. ServerCommunicationLink. model. Azuressqlservercommunicationlinkmodel</span><span class="sxs-lookup"><span data-stu-id="f4be0-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="f4be0-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4be0-137">NOTES</span></span>
* <span data-ttu-id="f4be0-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="f4be0-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="f4be0-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4be0-139">RELATED LINKS</span></span>

[<span data-ttu-id="f4be0-140">Yeni-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="f4be0-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="f4be0-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="f4be0-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="f4be0-142">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="f4be0-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)