---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 30a1599468851da5f01e10dc94af6586d3ecaf8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763380"
---
# <span data-ttu-id="1764b-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1764b-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="1764b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1764b-102">SYNOPSIS</span></span>
<span data-ttu-id="1764b-103">Belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1764b-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1764b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1764b-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1764b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1764b-105">DESCRIPTION</span></span>
<span data-ttu-id="1764b-106">**Set-AzureRmDataLakeStoreFirewallRule** cmdlet 'ı belirtilen veri</span><span class="sxs-lookup"><span data-stu-id="1764b-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="1764b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1764b-107">EXAMPLES</span></span>

### <span data-ttu-id="1764b-108">Örnek 1: güvenlik duvarı kuralı için başlangıç ve bitiş IP aralığını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1764b-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="1764b-109">"ContosoADL" hesabındaki "MyFirewallRule" güvenlik duvarı</span><span class="sxs-lookup"><span data-stu-id="1764b-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="1764b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1764b-110">PARAMETERS</span></span>

### <span data-ttu-id="1764b-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="1764b-111">-Account</span></span>
<span data-ttu-id="1764b-112">Güvenlik duvarı kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1764b-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="1764b-113">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="1764b-113">-EndIpAddress</span></span>
<span data-ttu-id="1764b-114">Güvenlik duvarı kuralı için geçerli IP aralığının sonu</span><span class="sxs-lookup"><span data-stu-id="1764b-114">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="1764b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="1764b-115">-Name</span></span>
<span data-ttu-id="1764b-116">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="1764b-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="1764b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1764b-117">-ResourceGroupName</span></span>
<span data-ttu-id="1764b-118">Güvenlik duvarı kuralını güncelleştirme hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1764b-118">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="1764b-119">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="1764b-119">-StartIpAddress</span></span>
<span data-ttu-id="1764b-120">Güvenlik duvarı kuralı için geçerli IP aralığının başlangıcı</span><span class="sxs-lookup"><span data-stu-id="1764b-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="1764b-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="1764b-121">-Confirm</span></span>
<span data-ttu-id="1764b-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1764b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1764b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1764b-123">-WhatIf</span></span>
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

### <span data-ttu-id="1764b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1764b-124">-DefaultProfile</span></span>
<span data-ttu-id="1764b-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1764b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1764b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1764b-126">CommonParameters</span></span>
<span data-ttu-id="1764b-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1764b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1764b-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1764b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1764b-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1764b-129">INPUTS</span></span>

## <span data-ttu-id="1764b-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1764b-130">OUTPUTS</span></span>

### <span data-ttu-id="1764b-131">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1764b-131">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="1764b-132">Güncelleştirilmiş güvenlik duvarı kuralının ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="1764b-132">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="1764b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1764b-133">NOTES</span></span>

## <span data-ttu-id="1764b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1764b-134">RELATED LINKS</span></span>

