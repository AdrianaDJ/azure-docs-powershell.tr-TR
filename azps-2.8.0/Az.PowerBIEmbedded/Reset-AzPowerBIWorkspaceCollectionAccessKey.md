---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: a6cef2f6b53061732cdbbf2875f35f573b532919
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932801"
---
# <span data-ttu-id="2e539-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="2e539-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="2e539-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e539-102">SYNOPSIS</span></span>
<span data-ttu-id="2e539-103">Belirtilen Access tuşunu sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="2e539-103">Resets the specified access key.</span></span>

## <span data-ttu-id="2e539-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e539-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e539-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e539-105">DESCRIPTION</span></span>
<span data-ttu-id="2e539-106">**Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet 'ı Power BI çalışma alanı koleksiyonunuzda belirtilen Access tuşunu sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="2e539-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="2e539-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e539-107">EXAMPLES</span></span>

### <span data-ttu-id="2e539-108">Örnek 1: birincil erişim anahtarını sıfırlama</span><span class="sxs-lookup"><span data-stu-id="2e539-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="2e539-109">Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonu için birincil erişim anahtarını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="2e539-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="2e539-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e539-110">PARAMETERS</span></span>

### <span data-ttu-id="2e539-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e539-111">-DefaultProfile</span></span>
<span data-ttu-id="2e539-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2e539-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e539-113">-Anahtar</span><span class="sxs-lookup"><span data-stu-id="2e539-113">-Key1</span></span>
<span data-ttu-id="2e539-114">Bu cmdlet 'in birincil erişim anahtarını sıfırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e539-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="2e539-115">-Anahtar2</span><span class="sxs-lookup"><span data-stu-id="2e539-115">-Key2</span></span>
<span data-ttu-id="2e539-116">Bu cmdlet 'in ikincil erişim tuşunu sıfırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e539-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="2e539-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e539-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e539-118">Koleksiyonun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e539-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="2e539-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="2e539-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="2e539-120">Bu cmdlet 'in üzerinde çalıştırıldığı Power BI çalışma alanı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e539-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e539-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e539-121">-Confirm</span></span>
<span data-ttu-id="2e539-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2e539-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e539-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e539-123">-WhatIf</span></span>
<span data-ttu-id="2e539-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e539-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e539-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2e539-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e539-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e539-126">CommonParameters</span></span>
<span data-ttu-id="2e539-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e539-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e539-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e539-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e539-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e539-129">INPUTS</span></span>

### <span data-ttu-id="2e539-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2e539-130">System.String</span></span>

## <span data-ttu-id="2e539-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e539-131">OUTPUTS</span></span>

### <span data-ttu-id="2e539-132">Microsoft. Azure. Commands. Management. PowerBIEmbedded. model. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="2e539-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="2e539-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e539-133">NOTES</span></span>

## <span data-ttu-id="2e539-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e539-134">RELATED LINKS</span></span>

[<span data-ttu-id="2e539-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="2e539-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


