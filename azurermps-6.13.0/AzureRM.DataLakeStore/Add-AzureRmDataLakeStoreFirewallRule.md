---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: d990f36fc68878a1751ad41ccfde51e4bbd82d2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591991"
---
# <span data-ttu-id="3d9b7-101">Add-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3d9b7-101">Add-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="3d9b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d9b7-102">SYNOPSIS</span></span>
<span data-ttu-id="3d9b7-103">Belirtilen Data Lake Store hesabına bir güvenlik duvarı kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="3d9b7-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d9b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d9b7-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d9b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d9b7-105">DESCRIPTION</span></span>
<span data-ttu-id="3d9b7-106">**Add-AzureRmDataLakeStoreFirewallRule** cmdlet 'ı belirtilen Data Lake Store hesabına bir güvenlik duvarı kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="3d9b7-106">The **Add-AzureRmDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="3d9b7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d9b7-107">EXAMPLES</span></span>

### <span data-ttu-id="3d9b7-108">Örnek 1: veri Lake Store hesabına yeni bir güvenlik duvarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="3d9b7-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="3d9b7-109">Bu, "ContosoADL" hesabında "ContosoADL" adlı, 127.0.0.1-127.0.0.2 adlı yeni bir güvenlik duvarı kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="3d9b7-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="3d9b7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d9b7-110">PARAMETERS</span></span>

### <span data-ttu-id="3d9b7-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="3d9b7-111">-Account</span></span>
<span data-ttu-id="3d9b7-112">Güvenlik duvarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="3d9b7-112">The Data Lake Store account to add the firewall rule to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d9b7-113">-DefaultProfile</span></span>
<span data-ttu-id="3d9b7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3d9b7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d9b7-115">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="3d9b7-115">-EndIpAddress</span></span>
<span data-ttu-id="3d9b7-116">Güvenlik duvarı kuralı için geçerli IP aralığının sonu</span><span class="sxs-lookup"><span data-stu-id="3d9b7-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9b7-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d9b7-117">-Name</span></span>
<span data-ttu-id="3d9b7-118">Eklenecek güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="3d9b7-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="3d9b7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d9b7-119">-ResourceGroupName</span></span>
<span data-ttu-id="3d9b7-120">Güvenlik duvarı kuralının ekleneceği hesabın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3d9b7-120">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9b7-121">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="3d9b7-121">-StartIpAddress</span></span>
<span data-ttu-id="3d9b7-122">Güvenlik duvarı kuralı için geçerli IP aralığının başlangıcı</span><span class="sxs-lookup"><span data-stu-id="3d9b7-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="3d9b7-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d9b7-123">-Confirm</span></span>
<span data-ttu-id="3d9b7-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d9b7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d9b7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d9b7-125">-WhatIf</span></span>
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

### <span data-ttu-id="3d9b7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d9b7-126">CommonParameters</span></span>
<span data-ttu-id="3d9b7-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d9b7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d9b7-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d9b7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d9b7-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d9b7-129">INPUTS</span></span>

### <span data-ttu-id="3d9b7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3d9b7-130">System.String</span></span>

## <span data-ttu-id="3d9b7-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d9b7-131">OUTPUTS</span></span>

### <span data-ttu-id="3d9b7-132">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3d9b7-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="3d9b7-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d9b7-133">NOTES</span></span>

## <span data-ttu-id="3d9b7-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d9b7-134">RELATED LINKS</span></span>