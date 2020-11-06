---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
ms.openlocfilehash: 409a1eca9083c51f501293e4ca37150ce0c328e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591170"
---
# <span data-ttu-id="a9930-101">Remove-AzureRmAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="a9930-101">Remove-AzureRmAutomationConnectionType</span></span>

## <span data-ttu-id="a9930-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9930-102">SYNOPSIS</span></span>
<span data-ttu-id="a9930-103">Otomasyon bağlantı türünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a9930-103">Removes an Automation connection type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9930-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9930-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9930-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9930-105">DESCRIPTION</span></span>
<span data-ttu-id="a9930-106">**Remove-AzureRmAutomationConnectionType** cmdlet 'ı Azure Otomasyonu 'ndan bağlantı türünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a9930-106">The **Remove-AzureRmAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>

<span data-ttu-id="a9930-107">Sildiğiniz bağlantı türüyle ilişkili tüm bağlantılar kullanılamaz duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="a9930-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="a9930-108">Aşağıdaki ölçütlere uyan yeni bir bağlantı türü oluşturmadıkça bunları kaldırın:</span><span class="sxs-lookup"><span data-stu-id="a9930-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 

- <span data-ttu-id="a9930-109">Türün adı, özgün bağlantı türüyle aynı.</span><span class="sxs-lookup"><span data-stu-id="a9930-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="a9930-110">Tür, özgün bağlantı türüyle aynı alan tanımlarına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="a9930-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="a9930-111">Ek alanlar olabilir.</span><span class="sxs-lookup"><span data-stu-id="a9930-111">It can have additional fields.</span></span>

## <span data-ttu-id="a9930-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9930-112">EXAMPLES</span></span>

### <span data-ttu-id="a9930-113">Örnek 1: bağlantı türünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="a9930-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzureRmAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a9930-114">Bu komut, Contoso17 adlı Otomasyon hesabında ContosoConnectionType adlı bir bağlantı türünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a9930-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a9930-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9930-115">PARAMETERS</span></span>

### <span data-ttu-id="a9930-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a9930-116">-AutomationAccountName</span></span>
<span data-ttu-id="a9930-117">Bu cmdlet 'in bağlantı türünü kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9930-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="a9930-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a9930-118">-Force</span></span>
<span data-ttu-id="a9930-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="a9930-119">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9930-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9930-120">-Name</span></span>
<span data-ttu-id="a9930-121">Bu cmdlet 'in kaldırıldığı Otomasyon bağlantı türünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9930-121">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a9930-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9930-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9930-123">Bu cmdlet 'in Otomasyon bağlantı türünü kaldıran kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9930-123">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="a9930-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9930-124">-Confirm</span></span>
<span data-ttu-id="a9930-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9930-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9930-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9930-126">-WhatIf</span></span>
<span data-ttu-id="a9930-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9930-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9930-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9930-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9930-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9930-129">-DefaultProfile</span></span>
<span data-ttu-id="a9930-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9930-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9930-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9930-131">CommonParameters</span></span>
<span data-ttu-id="a9930-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9930-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9930-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9930-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9930-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9930-134">INPUTS</span></span>

## <span data-ttu-id="a9930-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9930-135">OUTPUTS</span></span>

## <span data-ttu-id="a9930-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9930-136">NOTES</span></span>

## <span data-ttu-id="a9930-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9930-137">RELATED LINKS</span></span>

[<span data-ttu-id="a9930-138">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a9930-138">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


