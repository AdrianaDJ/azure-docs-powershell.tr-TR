---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/enable-azurermsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Enable-AzureRmSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Enable-AzureRmSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: 1276ba100a795ca113f1f09064bc46dfdfddf39b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764113"
---
# <span data-ttu-id="fd678-101">Enable-AzureRmSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="fd678-101">Enable-AzureRmSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="fd678-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd678-102">SYNOPSIS</span></span>
<span data-ttu-id="fd678-103">Sunucuda Gelişmiş tehdit korumasını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="fd678-103">Enables Advanced Threat Protection on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd678-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd678-104">SYNTAX</span></span>

```
Enable-AzureRmSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd678-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd678-105">DESCRIPTION</span></span>
<span data-ttu-id="fd678-106">**Enable-AzureRmSqlServerAdvancedThreatProtection** cmdlet 'ı sunucuda Gelişmiş tehdit korumasını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="fd678-106">The **Enable-AzureRmSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="fd678-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd678-107">EXAMPLES</span></span>

### <span data-ttu-id="fd678-108">Örnek 1-sunucu Gelişmiş tehdit korumasını etkinleştir</span><span class="sxs-lookup"><span data-stu-id="fd678-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzureRmSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="fd678-109">Örnek 2-sunucu kaynağından Gelişmiş tehdit korumasını etkinleştir</span><span class="sxs-lookup"><span data-stu-id="fd678-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzureRmSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="fd678-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd678-110">PARAMETERS</span></span>

### <span data-ttu-id="fd678-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd678-111">-DefaultProfile</span></span>
<span data-ttu-id="fd678-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd678-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd678-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd678-113">-InputObject</span></span>
<span data-ttu-id="fd678-114">Gelişmiş tehdit koruması ilke işlemiyle kullanılacak sunucu nesnesi</span><span class="sxs-lookup"><span data-stu-id="fd678-114">The server object to use with Advanced Threat Protection policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd678-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd678-115">-ResourceGroupName</span></span>
<span data-ttu-id="fd678-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fd678-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="fd678-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fd678-117">-ServerName</span></span>
<span data-ttu-id="fd678-118">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="fd678-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="fd678-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd678-119">-Confirm</span></span>
<span data-ttu-id="fd678-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd678-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd678-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd678-121">-WhatIf</span></span>
<span data-ttu-id="fd678-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd678-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd678-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd678-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd678-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd678-124">CommonParameters</span></span>
<span data-ttu-id="fd678-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd678-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd678-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd678-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd678-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd678-127">INPUTS</span></span>

### <span data-ttu-id="fd678-128">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="fd678-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="fd678-129">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd678-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="fd678-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fd678-130">System.String</span></span>

## <span data-ttu-id="fd678-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd678-131">OUTPUTS</span></span>

### <span data-ttu-id="fd678-132">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fd678-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="fd678-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd678-133">NOTES</span></span>

## <span data-ttu-id="fd678-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd678-134">RELATED LINKS</span></span>
