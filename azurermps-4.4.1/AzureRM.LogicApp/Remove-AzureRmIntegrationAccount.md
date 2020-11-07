---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
ms.openlocfilehash: eb78395274171f448076a4cd3ad9b6bac0093301
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765164"
---
# <span data-ttu-id="3c1be-101">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3c1be-101">Remove-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="3c1be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c1be-102">SYNOPSIS</span></span>
<span data-ttu-id="3c1be-103">Tümleştirme hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c1be-103">Removes an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c1be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c1be-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c1be-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c1be-105">DESCRIPTION</span></span>
<span data-ttu-id="3c1be-106">**Remove-AzureRmIntegrationAccount** cmdlet 'i, bir kaynak grubundan tümleştirme hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c1be-106">The **Remove-AzureRmIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="3c1be-107">Tümleştirme hesap adını ve kaynak grup adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3c1be-107">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="3c1be-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="3c1be-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3c1be-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="3c1be-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3c1be-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="3c1be-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3c1be-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="3c1be-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3c1be-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c1be-112">EXAMPLES</span></span>

### <span data-ttu-id="3c1be-113">Örnek 1: Tümleştirme hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3c1be-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="3c1be-114">Bu komut, IntegrationAccount31 adlı bir tümleştirme hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c1be-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="3c1be-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c1be-115">PARAMETERS</span></span>

### <span data-ttu-id="3c1be-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3c1be-116">-Force</span></span>
<span data-ttu-id="3c1be-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3c1be-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c1be-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="3c1be-118">-Name</span></span>
<span data-ttu-id="3c1be-119">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c1be-119">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1be-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c1be-120">-ResourceGroupName</span></span>
<span data-ttu-id="3c1be-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c1be-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3c1be-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="3c1be-122">-Confirm</span></span>
<span data-ttu-id="3c1be-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3c1be-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c1be-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c1be-124">-WhatIf</span></span>
<span data-ttu-id="3c1be-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c1be-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c1be-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3c1be-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c1be-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c1be-127">-DefaultProfile</span></span>
<span data-ttu-id="3c1be-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c1be-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c1be-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c1be-129">CommonParameters</span></span>
<span data-ttu-id="3c1be-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c1be-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c1be-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c1be-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c1be-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c1be-132">INPUTS</span></span>

## <span data-ttu-id="3c1be-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c1be-133">OUTPUTS</span></span>

## <span data-ttu-id="3c1be-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c1be-134">NOTES</span></span>

## <span data-ttu-id="3c1be-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c1be-135">RELATED LINKS</span></span>

[<span data-ttu-id="3c1be-136">Yeni-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3c1be-136">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="3c1be-137">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3c1be-137">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)

[<span data-ttu-id="3c1be-138">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3c1be-138">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)


