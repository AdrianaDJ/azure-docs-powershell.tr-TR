---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 4f9abf17be9b90cb4650c6f38748702dc0955b9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589659"
---
# <span data-ttu-id="cffd0-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="cffd0-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="cffd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cffd0-102">SYNOPSIS</span></span>
<span data-ttu-id="cffd0-103">İki sunucu arasındaki elastik veritabanı işlemleri için iletişim bağlantısını siler.</span><span class="sxs-lookup"><span data-stu-id="cffd0-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cffd0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cffd0-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cffd0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cffd0-105">DESCRIPTION</span></span>
<span data-ttu-id="cffd0-106">**Remove-AzureRmSqlServerCommunicationLink** cmdlet 'ı, Azure SQL veritabanındaki elastik veritabanı işlemleri için sunucudan sunucuya iletişim bağlantısını siler.</span><span class="sxs-lookup"><span data-stu-id="cffd0-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="cffd0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cffd0-107">EXAMPLES</span></span>

### <span data-ttu-id="cffd0-108">Örnek 1: iletişim bağlantısını silme</span><span class="sxs-lookup"><span data-stu-id="cffd0-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="cffd0-109">Bu komut, ContosoServer17 'da Link01 adlı sunucudan sunucuya iletişim bağlantısını siler.</span><span class="sxs-lookup"><span data-stu-id="cffd0-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="cffd0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cffd0-110">PARAMETERS</span></span>

### <span data-ttu-id="cffd0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cffd0-111">-DefaultProfile</span></span>
<span data-ttu-id="cffd0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cffd0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cffd0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cffd0-113">-Force</span></span>
<span data-ttu-id="cffd0-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="cffd0-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffd0-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="cffd0-115">-LinkName</span></span>
<span data-ttu-id="cffd0-116">Bu cmdlet 'in sildiği sunucu iletişim bağlantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cffd0-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffd0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cffd0-117">-ResourceGroupName</span></span>
<span data-ttu-id="cffd0-118">*ServerName* parametresi tarafından belirtilen sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cffd0-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="cffd0-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cffd0-119">-ServerName</span></span>
<span data-ttu-id="cffd0-120">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cffd0-120">Specifies the name of a server.</span></span>
<span data-ttu-id="cffd0-121">Bu sunucu, bu cmdlet 'in sildiği iletişim bağlantısını içerir.</span><span class="sxs-lookup"><span data-stu-id="cffd0-121">This server contains the communication link that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffd0-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="cffd0-122">-Confirm</span></span>
<span data-ttu-id="cffd0-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cffd0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cffd0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cffd0-124">-WhatIf</span></span>
<span data-ttu-id="cffd0-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cffd0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cffd0-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cffd0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cffd0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cffd0-127">CommonParameters</span></span>
<span data-ttu-id="cffd0-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cffd0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cffd0-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cffd0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cffd0-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cffd0-130">INPUTS</span></span>

### <span data-ttu-id="cffd0-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cffd0-131">None</span></span>
<span data-ttu-id="cffd0-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="cffd0-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cffd0-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cffd0-133">OUTPUTS</span></span>

### <span data-ttu-id="cffd0-134">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservercommunicationlinkmodel</span><span class="sxs-lookup"><span data-stu-id="cffd0-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="cffd0-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cffd0-135">NOTES</span></span>
* <span data-ttu-id="cffd0-136">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="cffd0-136">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="cffd0-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cffd0-137">RELATED LINKS</span></span>

[<span data-ttu-id="cffd0-138">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="cffd0-138">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="cffd0-139">Yeni-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="cffd0-139">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="cffd0-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="cffd0-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
