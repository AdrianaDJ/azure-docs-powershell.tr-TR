---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5b65e7f1dde9a4fc75e67b11cf4b7692a174add0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591977"
---
# <span data-ttu-id="eb845-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eb845-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="eb845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb845-102">SYNOPSIS</span></span>
<span data-ttu-id="eb845-103">Belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="eb845-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb845-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb845-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb845-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb845-105">DESCRIPTION</span></span>
<span data-ttu-id="eb845-106">**Set-AzureRmDataLakeStoreFirewallRule** cmdlet 'ı belirtilen veri</span><span class="sxs-lookup"><span data-stu-id="eb845-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="eb845-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb845-107">EXAMPLES</span></span>

### <span data-ttu-id="eb845-108">Örnek 1: güvenlik duvarı kuralı için başlangıç ve bitiş IP aralığını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="eb845-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="eb845-109">"ContosoADL" hesabındaki "MyFirewallRule" güvenlik duvarı</span><span class="sxs-lookup"><span data-stu-id="eb845-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="eb845-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb845-110">PARAMETERS</span></span>

### <span data-ttu-id="eb845-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="eb845-111">-Account</span></span>
<span data-ttu-id="eb845-112">Güvenlik duvarı kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="eb845-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="eb845-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb845-113">-DefaultProfile</span></span>
<span data-ttu-id="eb845-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="eb845-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb845-115">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="eb845-115">-EndIpAddress</span></span>
<span data-ttu-id="eb845-116">Güvenlik duvarı kuralı için geçerli IP aralığının sonu</span><span class="sxs-lookup"><span data-stu-id="eb845-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb845-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="eb845-117">-Name</span></span>
<span data-ttu-id="eb845-118">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="eb845-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="eb845-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb845-119">-ResourceGroupName</span></span>
<span data-ttu-id="eb845-120">Güvenlik duvarı kuralını güncelleştirme hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb845-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb845-121">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="eb845-121">-StartIpAddress</span></span>
<span data-ttu-id="eb845-122">Güvenlik duvarı kuralı için geçerli IP aralığının başlangıcı</span><span class="sxs-lookup"><span data-stu-id="eb845-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="eb845-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb845-123">-Confirm</span></span>
<span data-ttu-id="eb845-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb845-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb845-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb845-125">-WhatIf</span></span>
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

### <span data-ttu-id="eb845-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb845-126">CommonParameters</span></span>
<span data-ttu-id="eb845-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb845-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb845-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb845-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb845-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb845-129">INPUTS</span></span>

### <span data-ttu-id="eb845-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eb845-130">System.String</span></span>

## <span data-ttu-id="eb845-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb845-131">OUTPUTS</span></span>

### <span data-ttu-id="eb845-132">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eb845-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="eb845-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb845-133">NOTES</span></span>

## <span data-ttu-id="eb845-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb845-134">RELATED LINKS</span></span>
