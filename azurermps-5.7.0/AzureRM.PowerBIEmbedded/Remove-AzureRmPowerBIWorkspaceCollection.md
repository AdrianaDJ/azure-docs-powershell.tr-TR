---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7f3a48db5d8f1e6c7b4b0e73b705fc375a0b514f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764019"
---
# <span data-ttu-id="f996f-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f996f-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="f996f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f996f-102">SYNOPSIS</span></span>
<span data-ttu-id="f996f-103">Power BI çalışma alanı koleksiyonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f996f-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f996f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f996f-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f996f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f996f-105">DESCRIPTION</span></span>
<span data-ttu-id="f996f-106">**Remove-AzureRmPowerBIWorkspaceCollection** cmdlet 'ı, Azure aboneliğinizden ve kaynak Grupunuzdan Power BI çalışma alanı koleksiyonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f996f-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="f996f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f996f-107">EXAMPLES</span></span>

### <span data-ttu-id="f996f-108">Örnek 1: çalışma alanı koleksiyonunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="f996f-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="f996f-109">Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f996f-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="f996f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f996f-110">PARAMETERS</span></span>

### <span data-ttu-id="f996f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f996f-111">-DefaultProfile</span></span>
<span data-ttu-id="f996f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f996f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f996f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f996f-113">-ResourceGroupName</span></span>
<span data-ttu-id="f996f-114">Bu cmdlet 'in çalışma alanı koleksiyonunu kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f996f-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="f996f-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="f996f-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="f996f-116">Bu cmdlet 'in kaldırıldığı Power BI çalışma alanı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f996f-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f996f-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="f996f-117">-Confirm</span></span>
<span data-ttu-id="f996f-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f996f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f996f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f996f-119">-WhatIf</span></span>
<span data-ttu-id="f996f-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f996f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f996f-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f996f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f996f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f996f-122">CommonParameters</span></span>
<span data-ttu-id="f996f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f996f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f996f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f996f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f996f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f996f-125">INPUTS</span></span>

### <span data-ttu-id="f996f-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f996f-126">None</span></span>
<span data-ttu-id="f996f-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f996f-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f996f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f996f-128">OUTPUTS</span></span>

## <span data-ttu-id="f996f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f996f-129">NOTES</span></span>

## <span data-ttu-id="f996f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f996f-130">RELATED LINKS</span></span>

[<span data-ttu-id="f996f-131">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f996f-131">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="f996f-132">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f996f-132">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


