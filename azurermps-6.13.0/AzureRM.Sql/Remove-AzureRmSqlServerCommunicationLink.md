---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 3d2137aa1398e5bb3b8173b6ea927c4deb50d41f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764593"
---
# <span data-ttu-id="57f43-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="57f43-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="57f43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57f43-102">SYNOPSIS</span></span>
<span data-ttu-id="57f43-103">İki sunucu arasındaki elastik veritabanı işlemleri için iletişim bağlantısını siler.</span><span class="sxs-lookup"><span data-stu-id="57f43-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57f43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57f43-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57f43-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="57f43-105">DESCRIPTION</span></span>
<span data-ttu-id="57f43-106">**Remove-AzureRmSqlServerCommunicationLink** cmdlet 'ı, Azure SQL veritabanındaki elastik veritabanı işlemleri için sunucudan sunucuya iletişim bağlantısını siler.</span><span class="sxs-lookup"><span data-stu-id="57f43-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="57f43-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57f43-107">EXAMPLES</span></span>

### <span data-ttu-id="57f43-108">Örnek 1: iletişim bağlantısını silme</span><span class="sxs-lookup"><span data-stu-id="57f43-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="57f43-109">Bu komut, ContosoServer17 'da Link01 adlı sunucudan sunucuya iletişim bağlantısını siler.</span><span class="sxs-lookup"><span data-stu-id="57f43-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="57f43-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57f43-110">PARAMETERS</span></span>

### <span data-ttu-id="57f43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f43-111">-DefaultProfile</span></span>
<span data-ttu-id="57f43-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="57f43-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57f43-113">-Force</span><span class="sxs-lookup"><span data-stu-id="57f43-113">-Force</span></span>
<span data-ttu-id="57f43-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="57f43-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="57f43-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="57f43-115">-LinkName</span></span>
<span data-ttu-id="57f43-116">Bu cmdlet 'in sildiği sunucu iletişim bağlantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57f43-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="57f43-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57f43-117">-ResourceGroupName</span></span>
<span data-ttu-id="57f43-118">*ServerName* parametresi tarafından belirtilen sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57f43-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="57f43-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="57f43-119">-ServerName</span></span>
<span data-ttu-id="57f43-120">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57f43-120">Specifies the name of a server.</span></span>
<span data-ttu-id="57f43-121">Bu sunucu, bu cmdlet 'in sildiği iletişim bağlantısını içerir.</span><span class="sxs-lookup"><span data-stu-id="57f43-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="57f43-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="57f43-122">-Confirm</span></span>
<span data-ttu-id="57f43-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="57f43-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57f43-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57f43-124">-WhatIf</span></span>
<span data-ttu-id="57f43-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57f43-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57f43-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="57f43-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57f43-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f43-127">CommonParameters</span></span>
<span data-ttu-id="57f43-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57f43-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f43-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57f43-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f43-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57f43-130">INPUTS</span></span>

### <span data-ttu-id="57f43-131">System. String</span><span class="sxs-lookup"><span data-stu-id="57f43-131">System.String</span></span>

## <span data-ttu-id="57f43-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57f43-132">OUTPUTS</span></span>

### <span data-ttu-id="57f43-133">Microsoft. Azure. Commands. Sql. ServerCommunicationLink. model. Azuressqlservercommunicationlinkmodel</span><span class="sxs-lookup"><span data-stu-id="57f43-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="57f43-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57f43-134">NOTES</span></span>
* <span data-ttu-id="57f43-135">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="57f43-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="57f43-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57f43-136">RELATED LINKS</span></span>

[<span data-ttu-id="57f43-137">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="57f43-137">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="57f43-138">Yeni-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="57f43-138">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="57f43-139">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="57f43-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
