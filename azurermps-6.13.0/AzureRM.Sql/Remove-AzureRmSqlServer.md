---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: a6afa65eaf77cbc30ba63485112c52114d6ddded
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763788"
---
# <span data-ttu-id="e386b-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="e386b-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="e386b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e386b-102">SYNOPSIS</span></span>
<span data-ttu-id="e386b-103">Azure SQL veritabanı sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e386b-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e386b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e386b-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e386b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e386b-105">DESCRIPTION</span></span>
<span data-ttu-id="e386b-106">**Remove-AzureRmSqlServer** cmdlet 'ı BIR Azure SQL veritabanı sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e386b-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="e386b-107">Silme işlemi zaman uyumsuzdur ve biraz zaman alabilir, bu nedenle tamamen silinen sunucuya bağlı olan ek işlemleri gerçekleştirmeden önce işlemin bitiryapıldığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e386b-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="e386b-108">Örneğin, aynı adı kullanan yeni bir sunucu oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e386b-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="e386b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e386b-109">EXAMPLES</span></span>

### <span data-ttu-id="e386b-110">Örnek 1: sunucu kaldırma</span><span class="sxs-lookup"><span data-stu-id="e386b-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="e386b-111">Bu komut, server01 adlı Azure SQL veritabanı sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e386b-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="e386b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e386b-112">PARAMETERS</span></span>

### <span data-ttu-id="e386b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e386b-113">-DefaultProfile</span></span>
<span data-ttu-id="e386b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e386b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e386b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e386b-115">-Force</span></span>
<span data-ttu-id="e386b-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e386b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e386b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e386b-117">-ResourceGroupName</span></span>
<span data-ttu-id="e386b-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e386b-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e386b-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e386b-119">-ServerName</span></span>
<span data-ttu-id="e386b-120">Kaldırılacak sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e386b-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e386b-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="e386b-121">-Confirm</span></span>
<span data-ttu-id="e386b-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e386b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e386b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e386b-123">-WhatIf</span></span>
<span data-ttu-id="e386b-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e386b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e386b-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e386b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e386b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e386b-126">CommonParameters</span></span>
<span data-ttu-id="e386b-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e386b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e386b-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e386b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e386b-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e386b-129">INPUTS</span></span>

### <span data-ttu-id="e386b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e386b-130">System.String</span></span>

## <span data-ttu-id="e386b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e386b-131">OUTPUTS</span></span>

### <span data-ttu-id="e386b-132">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="e386b-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="e386b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e386b-133">NOTES</span></span>

## <span data-ttu-id="e386b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e386b-134">RELATED LINKS</span></span>

[<span data-ttu-id="e386b-135">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="e386b-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="e386b-136">Yeni-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="e386b-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="e386b-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="e386b-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="e386b-138">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="e386b-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


