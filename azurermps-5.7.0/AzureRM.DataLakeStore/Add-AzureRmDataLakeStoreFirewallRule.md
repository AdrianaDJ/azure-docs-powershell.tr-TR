---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: c1e4c3f748df4808fe570e95150450d3b3987d00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594091"
---
# <span data-ttu-id="f8208-101">Add-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f8208-101">Add-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f8208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8208-102">SYNOPSIS</span></span>
<span data-ttu-id="f8208-103">Belirtilen Data Lake Store hesabına bir güvenlik duvarı kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="f8208-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8208-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8208-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8208-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8208-105">DESCRIPTION</span></span>
<span data-ttu-id="f8208-106">**Add-AzureRmDataLakeStoreFirewallRule** cmdlet 'ı belirtilen Data Lake Store hesabına bir güvenlik duvarı kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="f8208-106">The **Add-AzureRmDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="f8208-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8208-107">EXAMPLES</span></span>

### <span data-ttu-id="f8208-108">Örnek 1: veri Lake Store hesabına yeni bir güvenlik duvarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="f8208-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="f8208-109">Bu, "ContosoADL" hesabında "ContosoADL" adlı, 127.0.0.1-127.0.0.2 adlı yeni bir güvenlik duvarı kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="f8208-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="f8208-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8208-110">PARAMETERS</span></span>

### <span data-ttu-id="f8208-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="f8208-111">-Account</span></span>
<span data-ttu-id="f8208-112">Güvenlik duvarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="f8208-112">The Data Lake Store account to add the firewall rule to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8208-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8208-113">-DefaultProfile</span></span>
<span data-ttu-id="f8208-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f8208-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8208-115">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="f8208-115">-EndIpAddress</span></span>
<span data-ttu-id="f8208-116">Güvenlik duvarı kuralı için geçerli IP aralığının sonu</span><span class="sxs-lookup"><span data-stu-id="f8208-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8208-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f8208-117">-Name</span></span>
<span data-ttu-id="f8208-118">Eklenecek güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="f8208-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="f8208-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8208-119">-ResourceGroupName</span></span>
<span data-ttu-id="f8208-120">Güvenlik duvarı kuralının ekleneceği hesabın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f8208-120">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8208-121">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="f8208-121">-StartIpAddress</span></span>
<span data-ttu-id="f8208-122">Güvenlik duvarı kuralı için geçerli IP aralığının başlangıcı</span><span class="sxs-lookup"><span data-stu-id="f8208-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="f8208-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="f8208-123">-Confirm</span></span>
<span data-ttu-id="f8208-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f8208-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8208-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8208-125">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8208-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8208-126">CommonParameters</span></span>
<span data-ttu-id="f8208-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8208-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8208-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8208-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8208-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8208-129">INPUTS</span></span>

### <span data-ttu-id="f8208-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f8208-130">None</span></span>
<span data-ttu-id="f8208-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f8208-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8208-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8208-132">OUTPUTS</span></span>

### <span data-ttu-id="f8208-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f8208-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="f8208-134">Eklenen güvenlik duvarı kuralı.</span><span class="sxs-lookup"><span data-stu-id="f8208-134">The firewall rule that was added.</span></span>

## <span data-ttu-id="f8208-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8208-135">NOTES</span></span>

## <span data-ttu-id="f8208-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8208-136">RELATED LINKS</span></span>

